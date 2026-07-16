# Postman Pagination — PokéAPI

A Postman collection that automatically pages through a paginated API, using `pm.execution.setNextRequest()` to chain requests until the data runs out.

📄 [View live documentation](https://documenter.getpostman.com/view/54488922/2sBY4Mv254)

## What it does

- Sends an initial request and pulls the pagination URL (`next`) out of the JSON response body
- Chains into a second request that re-runs itself, advancing to the next page automatically
- Includes a hard stop so it doesn't loop forever

## Requests

| Request | Purpose |
|---|---|
| `Start Request` | starts the run, grabs page 1, pulls the `next` URL |
| `Fetch Next URL Request` | Re-runs itself against each subsequent page until `next` is null or the safety limit is hit |

## How to use it

1. Click **View live documentation** above, or import `Pagination Exercise PokéAPI` manually
2. No environment file needed or auth (PokéAPI is an open API) 
3. Open the Postman Console (`View → Show Postman Console`) to watch it run
4. Right-click collection → **Run collection**

---

**Built with:** [Postman](https://www.postman.com/) · [PokéAPI](https://pokeapi.co/) · [Claude](https://claude.ai/)
