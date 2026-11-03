# ManDarpan

## Run locally

Start the prediction API in one PowerShell window:

```powershell
python -m uvicorn main:app --reload --host 127.0.0.1 --port 2200
```

Serve the frontend from the `frontend` directory in a second window:

```powershell
python -m http.server 8000 --directory frontend
```

Open http://localhost:8000. The frontend calls the local API at port 2200.
On Vercel, the FastAPI app serves predictions and the frontend is delivered
from the same deployment.

## Deploy

Run `vercel --prod` from the project root to deploy the frontend and API together.
