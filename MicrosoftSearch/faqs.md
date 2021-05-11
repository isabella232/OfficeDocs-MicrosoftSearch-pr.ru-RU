---
title: Вопросы и ответы
ms.author: jeffkizn
author: jeffkizn
manager: parulm
ms.audience: Admin
ms.topic: reference
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Получите ответы на часто задаваемые вопросы о поиске в корпоративной среде и Поиске (Майкрософт)
ms.openlocfilehash: 614fa241f353533b1c1e181904eb961fd55d0dfa
ms.sourcegitcommit: ea784081bc9c3ae7981a87a493d3a74503859dda
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2021
ms.locfileid: "52306073"
---
<!-- markdownlint-disable no-trailing-punctuation -->
# <a name="frequently-asked-questions"></a><span data-ttu-id="8f949-103">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="8f949-103">Frequently asked questions</span></span>

<span data-ttu-id="8f949-104">Ниже перечислены наиболее распространенные вопросы.</span><span class="sxs-lookup"><span data-stu-id="8f949-104">Here's a list of the most common questions.</span></span>

> [!TIP]
> <span data-ttu-id="8f949-105">Вашего вопроса здесь нет?</span><span class="sxs-lookup"><span data-stu-id="8f949-105">Don't see your question answered here?</span></span> <span data-ttu-id="8f949-106">Задайте свой вопрос в разделе отзывов этой статьи.</span><span class="sxs-lookup"><span data-stu-id="8f949-106">Ask your question in this article's feedback.</span></span>

## <a name="is-advanced-query-understanding-supported"></a><span data-ttu-id="8f949-107">Поддерживается ли расширенное понимание запросов?</span><span class="sxs-lookup"><span data-stu-id="8f949-107">Is advanced query understanding supported?</span></span>

<span data-ttu-id="8f949-108">Да, Microsoft Search разбирает намерения запроса из более крупных фраз.</span><span class="sxs-lookup"><span data-stu-id="8f949-108">Yes, Microsoft Search parses query intent from larger phrases.</span></span> <span data-ttu-id="8f949-109">Эта функция использует ИИ, чтобы узнать распространенные лишние фразы, которые пользователи добавляют в свои запросы, которые не влияют на их намерения поиска.</span><span class="sxs-lookup"><span data-stu-id="8f949-109">This feature uses AI to learn common superfluous phrases users add to their queries that don't impact their search intent.</span></span> <span data-ttu-id="8f949-110">Например, когда пользователь ищет дополнительные данные о том, как изменить *пароль,* мы извлекаем менее важные слова из запроса и запускаем на основе соответствующих паролей, таких как пароль *изменения.*</span><span class="sxs-lookup"><span data-stu-id="8f949-110">For example, when a user searches for *tell me more about how to change my password*, we extract the less important words from the query and trigger based on the relevant ones like *change password*.</span></span>
  
<span data-ttu-id="8f949-111">Эта функция не переопределит ключевые слова, заданные в центре администрирования Microsoft 365 [администратора.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="8f949-111">This feature won't override keywords set in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
  
## <a name="can-you-search-for-files-on-premises"></a><span data-ttu-id="8f949-112">Можно ли искать локальные файлы?</span><span class="sxs-lookup"><span data-stu-id="8f949-112">Can you search for files on-premises?</span></span>

<span data-ttu-id="8f949-113">Да.</span><span class="sxs-lookup"><span data-stu-id="8f949-113">Yes.</span></span> <span data-ttu-id="8f949-114">Вы можете искать локальное SharePoint [файлы,](http://sharepoint.com/) если у вас есть гибридное развертывание SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8f949-114">You can search on-premises [SharePoint](http://sharepoint.com/) files if you have a hybrid deployment of SharePoint.</span></span>
  
## <a name="how-do-i-make-bing-the-default-search-engine-for-people-in-my-org"></a><span data-ttu-id="8f949-115">Как сделать Bing поисковой системой по умолчанию для пользователей в организации?</span><span class="sxs-lookup"><span data-stu-id="8f949-115">How do I make Bing the default search engine for people in my org?</span></span>

<span data-ttu-id="8f949-116">Вот инструкции по настройке поисковой системы по умолчанию, домашней страницы по умолчанию и браузера по умолчанию, чтобы предоставить пользователям лучший опыт работы с Microsoft Search [в Bing:](https://Bing.com)</span><span class="sxs-lookup"><span data-stu-id="8f949-116">Here's the instructions for setting the default search engine, default homepage, and default browser to give your users the best experience with Microsoft Search in [Bing](https://Bing.com):</span></span>

- [<span data-ttu-id="8f949-117">Настройка Microsoft Edge браузера по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f949-117">Set Microsoft Edge as your default browser</span></span>](/deployedge/edge-default-browser)
- [<span data-ttu-id="8f949-118">Установка Bing в качестве поисковой системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f949-118">Make Bing your default search engine</span></span>](set-default-search-engine.md)
- [<span data-ttu-id="8f949-119">Настройка Bing.com в качестве корпоративной домашней страницы</span><span class="sxs-lookup"><span data-stu-id="8f949-119">Set Bing.com as your enterprise homepage</span></span>](set-default-homepage.md)

## <a name="how-are-my-search-results-protected"></a><span data-ttu-id="8f949-120">Как защищаются мои результаты поиска?</span><span class="sxs-lookup"><span data-stu-id="8f949-120">How are my search results protected?</span></span>

<span data-ttu-id="8f949-121">Мы [Azure Active Directory](/azure/active-directory/) проверку подлинности для доступа к результатам из доверенных облаков.</span><span class="sxs-lookup"><span data-stu-id="8f949-121">We require [Azure Active Directory](/azure/active-directory/) authentication to access results from the Trusted Cloud.</span></span> <span data-ttu-id="8f949-122">Пользователи, прошедшие проверку подлинности, видят в результатах поиска только тот контент, к которому у них есть доступ.</span><span class="sxs-lookup"><span data-stu-id="8f949-122">Authenticated users only see content they have access to.</span></span> <span data-ttu-id="8f949-123">Поисковые запросы деидентифицированы, а [](https://Bing.com) журналы отделены от общедоступных Bing поиска при использовании Microsoft Search в Bing.</span><span class="sxs-lookup"><span data-stu-id="8f949-123">Search queries are de-identified, and logs are separated from public [Bing](https://Bing.com) search traffic when you use Microsoft Search in Bing.</span></span>

## <a name="can-i-search-across-federated-organizations"></a><span data-ttu-id="8f949-124">Можно ли выполнять поиск в разных федеративных организациях?</span><span class="sxs-lookup"><span data-stu-id="8f949-124">Can I search across federated organizations?</span></span>

<span data-ttu-id="8f949-125">Нет.</span><span class="sxs-lookup"><span data-stu-id="8f949-125">No.</span></span>

## <a name="where-can-i-get-info-about-office-365-security-compliance-and-privacy"></a><span data-ttu-id="8f949-126">Где можно получить сведения о Office 365 безопасности, соответствии требованиям и конфиденциальности?</span><span class="sxs-lookup"><span data-stu-id="8f949-126">Where can I get info about Office 365 security, compliance, and privacy?</span></span>

<span data-ttu-id="8f949-127">Подробные сведения можно найти на страницах Центра доверия [для Office 365.](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f949-127">Details can be found on the [Trust Center pages for Office 365](https://www.microsoft.com/TrustCenter/CloudServices/office365/default.aspx).</span></span>

## <a name="can-guest-users-leverage-microsoft-search-in-my-organization"></a><span data-ttu-id="8f949-128">Могут ли гостевых пользователей использовать Microsoft Search в моей организации?</span><span class="sxs-lookup"><span data-stu-id="8f949-128">Can guest users leverage Microsoft Search in my organization?</span></span>

<span data-ttu-id="8f949-129">Microsoft 365 позволяет тесно сотрудничать с людьми за пределами организации с помощью [гостевого доступа.](/microsoft-365/solutions/collaborate-with-people-outside-your-organization)</span><span class="sxs-lookup"><span data-stu-id="8f949-129">Microsoft 365 enables rich collaboration with people outside of your organization through [guest access.](/microsoft-365/solutions/collaborate-with-people-outside-your-organization)</span></span> <span data-ttu-id="8f949-130">Эти пользователи смогут выполнять операции поиска по документам, сайтам, группам, спискам и библиотекам.</span><span class="sxs-lookup"><span data-stu-id="8f949-130">These users will be able to perform search operations on documents, sites, groups, lists, and libraries.</span></span> <span data-ttu-id="8f949-131">Однако гостевых пользователей не будет получать полный, персонализированный, Microsoft Search и может потребоваться использовать поле поиска на странице вместо единого окна Поиска Майкрософт в загоне.</span><span class="sxs-lookup"><span data-stu-id="8f949-131">However, guest users will not get the full, personalized, Microsoft Search experience and may need to leverage the on-page search box instead of the unified Microsoft Search box in the header.</span></span>