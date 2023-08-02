```mermaid
sequenceDiagram
	participant Valuer
	participant Valuer-UI
	participant Connect
	Valuer->>Valuer-UI:Submit submitValuation form
	Valuer-UI->>Valuer-UI:Validate Form Fields
	Valuer-UI->>Valuer-UI:Mapping & Build SubmitValuation payload
	Valuer-UI->>Connect:Send submitValuationRequest
```
