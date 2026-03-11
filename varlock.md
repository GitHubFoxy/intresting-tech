https://varlock.dev/getting-started/introduction/

AI-safe .env

# Declarative schema — AI agents get full context, never secret values
# @sensitive @required @type=string(startsWith=sk-)
OPENAI_API_KEY=

# @type=enum(development, preview, production, test)
APP_ENV=development # set non-sensitive default values directly

# use function calls to securely fetch data from external sources
XYZ_TOKEN=exec('op read "op://api-prod/xyz/auth-token"')
