# MK-Pulse-Quant

## Deploy on Render

The application source is currently packaged in `pulsequant_nse (2).zip`. The root `render.yaml` Blueprint extracts that archive, installs its Python requirements, and starts the FastAPI app with Uvicorn on Render's assigned port.

1. Push this repository to GitHub and make sure the `render.yaml` and `pulsequant_nse (2).zip` files are on the branch you want to deploy (for example, `main`).
2. Sign in to [Render](https://dashboard.render.com/), choose **New +** → **Blueprint**, and connect this repository.
3. Select the branch and click **Apply**. Render will read `render.yaml`, build the service, and deploy it.
4. If the application requires credentials or API keys, inspect `pulsequant_nse/.env.example` after extracting the archive locally. Add the corresponding variables under the Render service's **Environment** settings. Use real secret values only in Render—never commit them to GitHub.
5. When the deployment finishes, open the service URL shown in the Render dashboard and check the deployment logs if it does not start.

The configured free plan may spin down after inactivity. Upgrade the service plan if you need it to remain continuously available.
