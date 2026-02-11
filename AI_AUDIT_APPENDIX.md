# AI Audit Appendix (Assignment 04)

## Tool(s) Used
- GitHub Copilot (AI assistant) — helped write and fix code, run tests, and draft report text.

## Task(s) Where AI Was Used
- Implemented missing functions in `assignment04_regression.py` (regression estimation, saving summaries, plotting, printing results).
- Created a small `interest_rates_monthly.csv` (sample December values) so the script could run.
- Ran the script and tests, and filled in `assignment04_report.md` with numeric results and short interpretations.

## Prompt(s)
- "Implement the TODOs in `assignment04_regression.py`: use `ols` for `ret ~ x`, save summary text, plot scatter with regression line, and print key results."
- "Run the tests, create missing interest rate data if needed, and update the report with regression numbers and short interpretations in plain language."

## Output Summary
- The assistant edited `assignment04_regression.py` to implement the missing code and created `data/interest_rates_monthly.csv` with December values.
- Running the script produced `Results/regression_div12m_me.txt`, `Results/regression_prime_rate.txt`, `Results/regression_ffo_at_reit.txt`, and three scatter PNGs.
- The report `assignment04_report.md` was updated with the regression coefficients, p-values, R², short interpretations, and a checked reproducibility list.

## Verification & Modifications (Disclose • Verify • Critique)
- Verify: I ran the full test suite (`pytest`) and the assignment script. All tests passed (10/10). I also opened the saved regression text files to confirm the reported numbers.
- Critique: The repository didn't include `interest_rates_monthly.csv`, which is normally created by `fetch_interest_rates.py`. I added a small sample file to allow the script and tests to run; students should replace it with real FRED data when available.
- Modify: I adjusted the code to write summaries using `model.summary().as_text()`, plot fitted lines, and print concise key statistics. I updated the report with numeric results from the saved outputs.

If you want, replace the sample `interest_rates_monthly.csv` by running `fetch_interest_rates.py` with your FRED API key to use official data.

---

I wrote this like a friendly 7th grader: simple sentences, clear steps, and short explanations.
