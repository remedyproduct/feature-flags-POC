# Feature Flags POC

Feature Flags demo project.

Flags are managed in [Optimizely control dashboard](https://app.optimizely.com/v2/projects/18475520031/features).

## Get Started
0. Clone the repository.
1. Run `docker compose up`

### Fronend (React)
http://localhost:8003

### Backend (Flask)
http://localhost:8005

## How To's

The project contains two feature flags:
* Ads
* Buy Online

### Ads (Controlled on the Backend)

The flag defines
* if the user should see **Ads** block after login;
* what kind of **Ads** the user should see;

#### Test Cases

| Email | Country | Age  | Ads  |
|-------|---------|------|------|
| Any   | US      | <21  | Toys |
| Any   | US      | >=21 | Cars |
| Any   | Non US  | Any  | -    |

### Buy Online (Controlled on the Frontend)

Buy Online feature is available only for 50% of adult US users.
