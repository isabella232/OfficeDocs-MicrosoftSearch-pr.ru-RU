---
title: Вопросы и ответы
ms.author: anfowler
author: adefowler
manager: shohara
ms.date: 10/19/2018
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Priority
search.appverid:
- BFB160
- MET150
- MOE150
ms.assetid: cd3ee09d-58ab-4b8a-8822-fa11a1399672
ROBOTS: NoIndex
description: Получите ответы на часто задаваемые вопросы о поиске в корпоративной среде и Поиске (Майкрософт)
ms.openlocfilehash: 3b30980c76915405767381fb3b6397468bdd1b68
ms.sourcegitcommit: c2c9e66af1038efd2849d578f846680851f9e5d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36639506"
---
# <a name="frequently-asked-questions"></a><span data-ttu-id="60e05-103">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="60e05-103">Frequently asked questions</span></span>

<span data-ttu-id="60e05-104">Ниже перечислены наиболее распространенные вопросы.</span><span class="sxs-lookup"><span data-stu-id="60e05-104">Here's a list of the most common questions.</span></span>

> [!TIP]
> <span data-ttu-id="60e05-105">Вашего вопроса здесь нет?</span><span class="sxs-lookup"><span data-stu-id="60e05-105">Don't see your question answered here?</span></span> <span data-ttu-id="60e05-106">Задайте свой вопрос в разделе отзывов этой статьи.</span><span class="sxs-lookup"><span data-stu-id="60e05-106">Ask your question in this article's feedback.</span></span>

## <a name="is-advanced-query-understanding-supported"></a><span data-ttu-id="60e05-107">Поддерживается ли расширенное понимание запросов?</span><span class="sxs-lookup"><span data-stu-id="60e05-107">Is advanced query understanding supported?</span></span>

<span data-ttu-id="60e05-p102">Да, Поиск (Майкрософт) выделяет цель запроса из больших фраз. Эта функция использует ИИ для изучения распространенных избыточных фраз, которые добавляются пользователями в запросы и не влияют на цель поиска. Например, когда пользователь выполняет поиск по запросу "дополнительные сведения о том, как изменить пароль", менее важные слова извлекаются из запроса, и вызов результата осуществляется с учетом релевантных слов, таких как "изменить пароль".</span><span class="sxs-lookup"><span data-stu-id="60e05-p102">Yes, Microsoft Search parses query intent from larger phrases. This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent. For example, when a user searches for 'tell me more about how to change my password please' we extract the less important words from the query and trigger based on the relevant ones like 'change password.'</span></span>
  
<span data-ttu-id="60e05-111">Эта функция не имеет приоритета над набором ключевых слов в Центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="60e05-111">This feature will not override keywords set in the Admin portal.</span></span>
  
## <a name="can-you-search-for-files-on-premises"></a><span data-ttu-id="60e05-112">Можно ли искать локальные файлы?</span><span class="sxs-lookup"><span data-stu-id="60e05-112">Can you search for files on-premises?</span></span>

<span data-ttu-id="60e05-113">Да.</span><span class="sxs-lookup"><span data-stu-id="60e05-113">Yes.</span></span> <span data-ttu-id="60e05-114">Вы можете искать локальные файлы SharePoint, если вы используете гибридное развертывание SharePoint.</span><span class="sxs-lookup"><span data-stu-id="60e05-114">You can search on-premises SharePoint files if you have a hybrid deployment of SharePoint.</span></span>
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a><span data-ttu-id="60e05-115">Как сделать Bing поисковой системой по умолчанию для пользователей в организации?</span><span class="sxs-lookup"><span data-stu-id="60e05-115">How do I make Bing the default search engine for people in my org?</span></span>

<span data-ttu-id="60e05-116">Ниже приведены инструкции по настройке поисковой системы по умолчанию, домашней страницы по умолчанию и браузера по умолчанию, чтобы ваши пользователи могли оптимально использовать возможности Поиска (Майкрософт) в Bing:</span><span class="sxs-lookup"><span data-stu-id="60e05-116">Here's the instructions for setting the default search engine, default homepage, and default browser to give your users the best experience with Microsoft Search in Bing:</span></span>

- [<span data-ttu-id="60e05-117">Настройка Microsoft Edge в качестве браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="60e05-117">Set Edge as your default browser</span></span>](set-default-browser.md)
- [<span data-ttu-id="60e05-118">Установка Bing в качестве поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="60e05-118">Make Bing your default search engine</span></span>](set-default-search-engine.md)
- [<span data-ttu-id="60e05-119">Настройка Bing.com в качестве корпоративной домашней страницы</span><span class="sxs-lookup"><span data-stu-id="60e05-119">Set Bing.com as your enterprise homepage</span></span>](set-default-homepage.md)

  
## <a name="how-are-my-search-results-protected"></a><span data-ttu-id="60e05-120">Как защищаются мои результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="60e05-120">How are my search results protected?</span></span>

<span data-ttu-id="60e05-121">Мы требуем проверки подлинности Azure Active Directory (AAD) для доступа к результатам из надежной облачной среды.</span><span class="sxs-lookup"><span data-stu-id="60e05-121">We require Azure Active Directory (AAD) authentication to access results from the Trusted Cloud.</span></span> <span data-ttu-id="60e05-122">Пользователи, прошедшие проверку подлинности, видят в результатах поиска только тот контент, к которому у них есть доступ.</span><span class="sxs-lookup"><span data-stu-id="60e05-122">Authenticated users only see content they have access to.</span></span> <span data-ttu-id="60e05-123">Поисковые запросы обезличиваются, а журналы отделяются от общедоступного поискового трафика Bing.</span><span class="sxs-lookup"><span data-stu-id="60e05-123">Search queries are de-identified and logs are separated from public Bing search traffic.</span></span> <span data-ttu-id="60e05-124">Подобный уровень защиты нигде больше в отрасли не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="60e05-124">This level of protection is unavailable anywhere else in the industry.</span></span>

## <a name="can-i-search-across-federated-organizations"></a><span data-ttu-id="60e05-125">Можно ли выполнять поиск в разных федеративных организациях?</span><span class="sxs-lookup"><span data-stu-id="60e05-125">Can I search across federated organizations?</span></span>

<span data-ttu-id="60e05-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="60e05-126">No.</span></span>

## <a name="where-can-i-get-info-about-office-365-and-microsoft-365-compliance-tiers-and-categories"></a><span data-ttu-id="60e05-127">Где можно получить дополнительные сведения об уровнях и категориях соответствия требованиям в Office 365 и Microsoft 365?</span><span class="sxs-lookup"><span data-stu-id="60e05-127">Where can I get info about Office 365 and Microsoft 365 compliance tiers and categories?</span></span>

<span data-ttu-id="60e05-128">Подробные сведения можно найти в статье [Инфраструктура соответствия отраслевым стандартам и нормативным требованиям](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (скачать PDF).</span><span class="sxs-lookup"><span data-stu-id="60e05-128">Details can be found in the [Compliance Framework for Industry Standards and Regulations](https://download.microsoft.com/download/B/2/7/B27B3EF3-8849-4C18-8BA4-5AD755728620/Compliance%20Framework_customer%20guidance.pdf) (PDF download).</span></span>