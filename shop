import telebot
from telebot import types

bot = telebot.TeleBot('8421453257:AAF_YKXHFdvXJLJUmbngj4AeJeFDXtBqOCE')  # Замените на актуальный токен



def get_main_keyboard():
    markup = types.ReplyKeyboardMarkup(resize_keyboard=True)
    markup.add(types.KeyboardButton('Продавец'))
    markup.add(types.KeyboardButton('Наличие товара и цена'))
    markup.add(types.KeyboardButton('ТГК с розыгрышами🎁 и новинками😮‍💨'))
    return markup



@bot.message_handler(commands=['price'])
def price_handler(message):
    bot.send_message(message.chat.id, '👇Ссылка на гугл диск с наличием и ценой товара👇')
    bot.send_message(message.chat.id, 'https://docs.google.com/spreadsheets/d/1ZH8X4VtBedcFFRLNd5uiq7cGeX4zXJ6rMbtQnY1vAZQ/edit?gid=0#gid=0')
    bot.send_message(message.chat.id, '👆Ссылка на гугл диск с наличием и ценой товара👆', reply_markup=get_main_keyboard())



@bot.message_handler(commands=['seller'])
def seller_handler(message):
    bot.send_message(message.chat.id, 'Свяжись с продавцом для покупки 👉 @seller_grodno', reply_markup=get_main_keyboard())


@bot.message_handler(commands=['telegramchannel'])
def donat_handler(message):
    bot.send_message(message.chat.id, 'Ссылка на вступление https://t.me/+gPU-1_SQVmxjY2Nh', reply_markup=get_main_keyboard())


# 🔽 Обработчик текстовых сообщений
@bot.message_handler(func=lambda message: message.text == 'Продавец')
def seller_button_handler(message):
    bot.send_message(message.chat.id, 'Свяжись с продавцом для покупки 👉 @seller_grodno')

@bot.message_handler(func=lambda message: message.text == 'Наличие товара и цена')
def price_button_handler(message):
    bot.send_message(message.chat.id, '👇Ссылка на гугл диск с наличием и ценой товара👇')
    bot.send_message(message.chat.id, 'https://docs.google.com/spreadsheets/d/1ZH8X4VtBedcFFRLNd5uiq7cGeX4zXJ6rMbtQnY1vAZQ/edit?gid=0#gid=0')
    bot.send_message(message.chat.id, '👆Ссылка на гугл диск с наличием и ценой товара👆')

@bot.message_handler(func=lambda message: message.text == 'ТГК с розыгрышами🎁 и новинками😮‍💨')
def donat_button_handler(message):
    bot.send_message(message.chat.id, 'Ссылка на вступление https://t.me/+gPU-1_SQVmxjY2Nh')

@bot.message_handler(func=lambda message: True)
def fallback_handler(message):
    bot.send_message(message.chat.id, 'Пожалуйста, выбери одну из кнопок ниже 👇', reply_markup=get_main_keyboard())

bot.remove_webhook()
bot.polling(non_stop=True)
