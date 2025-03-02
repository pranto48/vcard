# Онлайн визитка

> See also [documentation in English](readme.md) 👀.

[![Скриншоты](https://grigorykovalev.github.io/online-business-card/example/example.gif)](https://grigorykovalev.github.io/online-business-card/example/example.jpg)

> Пример [сайта цифровой визитки](https://grigorykovalev.github.io/online-business-card/).

- [Описание](#about)
- [Как пользоваться](#how-to-use)
	- [Скачайте шаблон сайта визитки](#download-business-card-website-template)
	- [Добавьте контактные данные](#add-contact-details)
	- [Добавьте аватар](#add-your-avatar)
	- [Изменените фон](#change-background)
	- [Создайте QR-код](#create-qr-code)
	- [Создайте сайт цифровой визитки](#create-digital-business-card-website)

<a name="about"></a>
## Описание

[Шаблон цифровой визитки](#download-business-card-website-template), который вы можете изменить и разместить на любом хостинге, в том числе на [GitHub Pages](https://docs.github.com/ru/pages), тогда сайт вашей электронной визитки будет доступен по адресу вида `username.github.io`, где `username` имя вашего пользователя.

Файлы в [папке сайта визитки](https://github.com/GrigoryKovalev/online-business-card) для базового использования:

- [`vcard.vcf`](#add-contact-details) - файл в текстовом формате [vCard](https://ru.wikipedia.org/wiki/VCard) для заполнения данными вашей электронной визитки. 
- [`avatar.jpg`](#add-your-avatar) - аватар для замены на ваше изображение.
- [`background.jpg`](#change-background) - фоновое изображение для замены на ваше изображение.
- [`qrcode.png`](#create-qr-code) - файл QR-кода, содержащий сылку на онлайн визитку, для замены на ваш файл.

<a name="how-to-use"></a>
## Как пользоваться

<a name="download-business-card-website-template"></a>
### Скачайте шаблон сайта визитки

Вы можете скачать файлы сайта визитки по [ссылке](https://github.com/GrigoryKovalev/online-business-card/archive/refs/heads/master.zip) или перейти в [папку сайта визитки](https://github.com/GrigoryKovalev/online-business-card) и скачать ZIP-архив, нажав кнопку `Code` справа над списком файлов, а затем - `Download ZIP`.

<a name="add-contact-details"></a>
### Добавьте контактные данные

Вы можете создать и экспортировать карточку с вашими контактными данными и аватором в [VCF-файл](https://ru.wikipedia.org/wiki/VCard) на вашем устройстве [Android](https://support.google.com/contacts/answer/7199294?hl=ru), [Apple](https://support.apple.com/ru-ru/guide/contacts/adrbdcfd32e6/mac) или с помощью онлайн-сервиса [vCard maker](https://vcardmaker.com/), а затем заменить файл `vcard.vcf` в [папке сайта визитки](https://github.com/GrigoryKovalev/online-business-card) на созданный вами с таким же названием.

Затем вы также сможете редактировать ваши контактные данные в файле `vcard.vcf` с помощью текстового редактора на компьютере (в Windows/Блокнот или macOS/TextEdit), а также изменить онлайн после [создания сайта визитки](#create-digital-business-card-website).

Ссылка на карточку с контактными данными отображается в левом верхнем углу аватара, при клике по которой на мобильном устройстве будет предложено создать новый контакт, заполненный значениями из всех полей файла `vcard.vcf`, а при клике по ссылке на компьютере вы сможете скачать файл и импортировать его в ваши контакты.

> Обязательно добавьте аватар в файл `vcard.vcf`, если хотите чтобы он добавлялся в адресную книгу.

На сайте визитке отображаются только следующие поля из файла `vcard.vcf`:

- **Full Name** - `FN:First Name Middle Name Last Name` (you can specify it not in full), which is also contained in the `N:Last Name;First Name;Middle Name;Prefix;` field.
- **Nickname** `NICKNAME:Arif Mahmud`.
- **Organization** - `ORG:your organization`. If a value is specified, it is displayed under the name instead of the alias, in which case the alias is displayed when the name is clicked.
- **`Email`** - `EMAIL;type=INTERNET;type=HOME;type=pref:mail@arifmahmud.com`. If multiple email addresses are specified (home, work, etc.), only the values of the first email address are displayed.
- **Phone** - `TEL;type=CELL;type=VOICE;type=pref:+88 01915822266`. If several phones are specified (cellular, home, work, etc.), only the values of the first phone are displayed.
- **Link** - `URL;type=pref:https://arifmahmud.com/`. Displayed when you click on the corresponding icon in the lower right corner of the avatar.
- **Note** - `NOTE:Brief information about yourself`. Can contain additional references starting with `https://` or `www.`, as well as the line break character `\n`. Displayed when you click on the corresponding icon in the bottom left corner of the avatar.
- **ID of social profiles** - ID (login, phone), full URL or empty value (to display non-clickable icon): 
	- `X-SOCIALPROFILE;type=WhatsApp:+8801915822266` - phone `+8801915822266` in `WhatsApp`.
	- `X-SOCIALPROFILE;type=Telegram:@pranto48` - ID `@pranto48` in `Telegram`.
	- `X-SOCIALPROFILE;type=Viber:+8801915822266` - Phone `+8801915822266` in `Viber`.
	- `X-SOCIALPROFILE;type=VK:username` - Username `username` in `VK`.
	- `X-SOCIALPROFILE;type=Facebook:`
	- `X-SOCIALPROFILE;type=Instagram:`
	- `X-SOCIALPROFILE;type=Twitter:`
	- `X-SOCIALPROFILE;type=Flickr:`
	- `X-SOCIALPROFILE;type=LinkedIn:`
	- `X-SOCIALPROFILE;type=GitHub:https://github.com/username` - link `https://github.com/username` to `GitHub`.

> С помощью онлайн-сервиса [vCard maker](https://vcardmaker.com/) вы не сможете добавить все указанные профили социальных сетей, в таком случае необходимо будет добавить их вручную, отредактировав файл `vcard.vcf` после экспорта.

<a name="add-your-avatar"></a>
### Добавьте аватар

Замените файл `avatar.jpg` в [папке сайта визитки](https://github.com/GrigoryKovalev/online-business-card) на изображение вашего аватара с таким же названием, шириной и высотой не менее `330px`, если высота будет больше чем ширина, то только по клику аватар будет отображаться полностью.

> Обрезать и преобразовать изображение в `JPG` вы можете, например, с помощью онлайн-сервиса [iLoveImg](https://www.iloveimg.com/ru), а придать художественный стиль вашей фотографии - с помощью приложения [Prisma](https://prisma-ai.com).

Удалите или лучше замените файл `favicon.ico` на изображение вашего значка для отображения его во вкладке браузера.

> Создать значок `favicon.ico` вы можете, например, с помощью онлайн сервиса [Favicon Generator](https://realfavicongenerator.net), загрузив изображение вашего аватара и скачав новый файл значка.

<a name="change-background"></a>
### Изменените фон

Замените файл `background.jpg` в [папке сайта визитки](https://github.com/GrigoryKovalev/online-business-card) на изображение вашего фона с таким же названием.

> Вы можете скачать обои на рабочий стол в качестве фона, например, с помощью онлайн-сервиса [Wallpapers.com](https://wallpapers.com).

По желанию вы можете не использовать фоновое изображение или наоборот, использовать его только в режиме отображения [QR-кода](#create-qr-code), для этого замените файл `index.html` в [папке сайта визитки](https://github.com/GrigoryKovalev/online-business-card) на один из файлов в директории `/example` (скопируйте и переименуйте файл в `index.html`):

- [`index.html`](https://grigorykovalev.github.io/online-business-card/example/index.html) - шаблон с фоном белого цвета и фоном черного цвета в режиме отображения QR-кода.
- [`index.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.background.html) - шаблон с фоном белого цвета и фоновым изображением в режиме отображения QR-кода.
- [`index.dark.html`](https://grigorykovalev.github.io/online-business-card/example/index.dark.html) - шаблон с фоном черного цвета и белым фоном в режиме отображения QR-кода.
- [`index.dark.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.dark.background.html) - стандартный шаблон с фоновым изображением и белым фоном в режиме отображения QR-кода.

Также вы можете изменить шрифт, скопировав один из файлов в директории `/example` с дополнительным вариантом шрифта из семейства [Roboto](https://fonts.google.com/?query=Christian+Robertson):

- Roboto Condensed: 

	- [`index.condensed.html`](https://grigorykovalev.github.io/online-business-card/example/index.condensed.html) - белый фон/черный фон в режиме QR-кода;
	- [`index.condensed.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.condensed.background.html) - белый фон/фоновое изображение в режиме QR-кода;
	- [`index.condensed.dark.html`](https://grigorykovalev.github.io/online-business-card/example/index.condensed.dark.html) - черный фон/белый фон в режиме QR-кода;
	- [`index.condensed.dark.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.condensed.dark.background.html) - фоновое изображение/белый фон в режиме QR-кода;
	
- Roboto Mono: 

	- [`index.mono.html`](https://grigorykovalev.github.io/online-business-card/example/index.mono.html) - белый фон/черный фон в режиме QR-кода; 
	- [`index.mono.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.mono.background.html) - белый фон/фоновое изображение в режиме QR-кода; 
	- [`index.mono.dark.html`](https://grigorykovalev.github.io/online-business-card/example/index.mono.dark.html) - черный фон/белый фон в режиме QR-кода; 
	- [`index.mono.dark.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.mono.dark.background.html) - фоновое изображение/белый фон в режиме QR-кода;
	
- Roboto Slab: 

	- [`index.slab.html`](https://grigorykovalev.github.io/online-business-card/example/index.slab.html) - белый фон/черный фон в режиме QR-кода;
	- [`index.slab.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.slab.background.html) - белый фон/фоновое изображение в режиме QR-кода; 
	- [`index.slab.dark.html`](https://grigorykovalev.github.io/online-business-card/example/index.slab.dark.html) - черный фон/белый фон в режиме QR-кода; 
	- [`index.slab.dark.background.html`](https://grigorykovalev.github.io/online-business-card/example/index.slab.dark.background.html) - фоновое изображение/белый фон в режиме QR-кода.

<a name="create-qr-code"></a>
### Создайте QR-код

Создайте QR-код со ссылкой на сайт вашей визитки, например, с помощью онлайн-сервиса [QRCode Monkey](https://www.qrcode-monkey.com) и замените файл `qrcode.png` в [папке сайта визитки](https://github.com/GrigoryKovalev/online-business-card) на изображение вашего QR-кода с таким же названием. 

> Вы можете создать и обновить QR-код после [создания сайта визитки](#create-digital-business-card-website).

QR-код отображается при клике на соответствующую иконку в правом верхнем углу аватара. В режиме отображения QR-кода фон меняется на белый цвет.

<a name="create-digital-business-card-website"></a>
### Создайте сайт цифровой визитки

[Зарегестрируйтесь бесплатно на GitHub](https://github.com/signup), затем создайте новый репозиторий (место хранения файлов) с именем соответствующем `username.github.io` (где `username` - ваше имя пользователя) и включите в настройках [Github Pages](https://docs.github.com/ru/pages/quickstart).

> После регистрации, нажмите в правом верхнем углу знак `+` и нажмите в открывшемся меню `New repository`. На странице создания репозитория в поле `Owner` выберите ваше имя пользователя и в поле `Repository name` в качестве имени репозитория напишите `username.github.io`, где вместо `username` впишите ваше имя пользователя (маленькими буквами), оставьте галочку в поле `Public`, ничего больше не выбирайте и нажмите кнопку `Create repository`. 
>
> На странице вашего репозитория перейдите по ссылке `uploading an existing file`, перетащите файлы сайта визитки с вашего компьютера в поле `choose your files` и нажмите кнопку `Commit changes` для загрузки файлов.
> 
> Для включения GitHub Pages перейдите в настройки репозитория, нажав `Settings` в меню под названием вашего репозитория, затем перейдите в раздел `Pages` в меню слева и в поле `Branch` поменяйте значение `none` на главную ветку `main`, оставьте выбранную корневую директорию `/root` и нажмите кнопку `Save`. Через несколько минут ваши файлы опубликуются и в разделе `Pages` на верху отобразиться ссылка на ваш сайт вида `username.github.io`. 

Теперь вы можете [управлять файлами сайта визитки с помощью GitHub](https://docs.github.com/ru/repositories/working-with-files/managing-files) - редактировать текстовые файлы (например, изменить файл `vcard.vcf` с вашими контактными данными), загружать новые (например, изображение QR-кода `qrcode.png`) и удалять старые (например, удалить директорию `/example`).
