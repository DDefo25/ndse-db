##Задание 1

- Запрос для вставки данных минимум о двух книгах в коллекцию books
    db.books.insertMany([
        { authors: [{ first: 'Лев', last: 'Толстой', middle: 'Николаевич' }], title: 'Война и мир', published: 1869 },
        { authors: [{ first: 'Федор', last: 'Достоевский', middle: 'Михайлович' }], title: 'Преступление и наказание', published: 1869 },
    ])

- Запрос для поиска полей документов коллекции books по полю title
    db.books.find( title: { $eq: 'Преступление и наказание' })

- Запрос для редактирования полей: description и authors коллекции books по _id записи.
    db.books.updateOne(
        { _id: 1213Fs32f },
        { $set: { 
            description: 'Роман-эпопея, описывающий русское общество в эпоху войн против Наполеона в 1805—1812 годах.', 
            authors[{ first: 'Лев', last: 'Толстой', middle: 'Николаевич' }],
        }},
    )