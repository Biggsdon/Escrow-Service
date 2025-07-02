# Escrow-Service
Acts as a neutral, trusted mediator during business transactions.
from telegram.ext import Updater, CommandHandler, ConversationHandler, MessageHandler, Filters

def start(update, context):
    update.message.reply_text("Welcome! Use /create_deal to begin.")

def create_deal(update, context):
    update.message.reply_text("Please enter deal details...")

def report(update, context):
    update.message.reply_text("Describe your issue and attach evidence.")

updater = Updater('YOUR_BOT_TOKEN')
dp = updater.dispatcher

dp.add_handler(CommandHandler("start", start))
dp.add_handler(CommandHandler("create_deal", create_deal))
dp.add_handler(CommandHandler("report", report))

updater.start_polling()
