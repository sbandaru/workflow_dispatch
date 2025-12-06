# workflow_dispatch

### "message": "Invalid request.\n\nNo more than 10 properties are allowed; 11 were supplied.", - SUCKS !!!
 
```bash
curl -L \
  -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer <redact>" \
  -H "X-GitHub-Api-Version: 2022-11-28" \
  https://api.github.com/repos/sbandaru/workflow_dispatch/actions/workflows/test-workflow-dispatch.yml/dispatches \
  -d '{
        "ref": "main",
        "inputs": {
          "test-input-1": "value1",
          "test-input-2": "value2",
          "test-input-3": "value3",
          "test-input-4": "value4",
          "test-input-5": "value5",
          "test-input-6": "value6",
          "test-input-7": "value7",
          "test-input-8": "value8",
          "test-input-9": "value9",
          "test-input-10": "value10",
          "test-input-11": "value11"
        }
      }'
{
  "message": "Invalid request.\n\nNo more than 10 properties are allowed; 11 were supplied.",
  "documentation_url": "https://docs.github.com/rest/actions/workflows#create-a-workflow-dispatch-event",
  "status": "422"
}
```
