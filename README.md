# GitGabCompound
GitGabMyAgent
https://docs.github.com/en/get-started/learning-about-github/githubs-plans
https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/verifying-your-email-address
https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication

Request Install
pip3 install python-telegram-bot
from telegram.ext import Updater, CommandHandler, MessageHandler, Filters

# Replace this with your API key
TELEGRAM_API_KEY = "123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11"

def start(update, context):
    update.message.reply_text("Hello! Welcome to MyCoolBot.")

def echo(update, context):
    update.message.reply_text(update.message.text)

def main():
    updater = Updater(TELEGRAM_API_KEY, use_context=True)
    dp = updater.dispatcher

    dp.add_handler(CommandHandler("start", start))
    dp.add_handler(MessageHandler(Filters.text & ~Filters.command, echo))

    updater.start_polling()
    updater.idle()

if __name__ == "__main__":
    main()

python3 my_bot.py


