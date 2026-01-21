# Other Languages Integration Guide

For languages without an official SDK, use the REST API directly via HTTP requests.

## cURL Template

```bash
curl 'https://api.scorable.ai/v1/judges/{judge_id}/execute/' \
  -H 'authorization: Api-Key your-api-key' \
  -H 'content-type: application/json' \
  --data-raw '{"response":"LLM output here","request":"User input here"}'
```

## Integration Points

- Insert evaluation code where LLM outputs are generated
- `response` parameter: The text you want to evaluate (required)
- `request` parameter: The input that prompted the response (optional but recommended)
- Use actual variables from your code, not static strings

## Result Format

```json
{
  "evaluator_results": [
    {
      "evaluator_name": "Accuracy",
      "score": 0.85,
      "justification": "The response correctly identifies..."
    }
  ]
}
```

Each evaluator returns:
- `score`: Float between 0-1 (higher is better)
- `justification`: Natural language explanation

## Adapting to Your Language

Use this template with your language's HTTP client library (e.g., `requests` in Python, `fetch` in JavaScript, `http` in Go, etc.).
