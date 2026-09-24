# Trazabilidad — Customer Search

| Requirement | SPEC / AC | Task | Implementation | Test / Evidence | Status | Notes |
|---|---|---|---|---|---|---|
| FR-01 | AC-01 | T-03, T-04 | `src/customer_search/search.py`, `cli.py` | `test_partial_name_search`, `test_partial_email_search`, `test_cli_prints_customer_fields` | OK | Un término consulta ambos campos. |
| FR-02 | AC-02 | T-03 | `src/customer_search/search.py` | `test_partial_name_search`, `test_partial_email_search` | OK | Subcadena no exacta. |
| FR-03 | AC-03 | T-03 | `src/customer_search/search.py` | `test_case_insensitive_and_trimmed` | OK | Se usa `casefold()`. |
| FR-04 | AC-04 | T-02, T-04 | `src/customer_search/models.py`, `cli.py` | `test_model_has_required_fields`, `test_cli_prints_customer_fields` | OK | Salida con ID, nombre y correo. |
| FR-05 | AC-05 | T-04 | `src/customer_search/search.py`, `cli.py` | `test_no_matches_returns_empty_list`, `test_cli_reports_no_matches` | OK | Salida válida, código 0. |
| FR-06 | AC-06 | T-04 | `src/customer_search/search.py`, `cli.py` | `test_empty_term_is_rejected`, `test_non_text_term_is_rejected`, `test_cli_rejects_blank_term`, `test_cli_requires_exactly_one_argument` | OK | Código 2 en CLI. |
| NFR-01 | AC-07 | T-05 | `tests/test_search.py`, `tests/test_cli.py` | `pytest -v`: 15 pruebas aprobadas | OK | Incluye orden y no duplicación. |
| NFR-02 | AC-08 | T-01, T-03, T-04 | `pyproject.toml`, `src/customer_search/` | Inspección de dependencias y `PYTHONPATH=src python3 -m customer_search ana` | OK | Solo biblioteca estándar al ejecutar. |
| NFR-03 | AC-09 | T-01, T-06 | `pyproject.toml`, `README.md` | Instalación editable y ejecución de `customer-search ana` en entorno virtual; revisión de README | OK | Python >=3.11 declarado. |

Las reglas adicionales de orden y no duplicación de `SPEC.md` se verifican con `test_partial_search_preserves_order` y `test_customer_matching_both_fields_is_not_duplicated`.
