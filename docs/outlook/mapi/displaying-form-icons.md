---
title: Anzeigen von Formular Symbolen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337044"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="b7c97-103">Anzeigen von Formular Symbolen</span><span class="sxs-lookup"><span data-stu-id="b7c97-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="b7c97-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7c97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7c97-105">Wenn Sie eine Liste von Nachrichten in einem Ordner anzeigen, ist es für Ihre Benutzer hilfreich, wenn Sie Nachrichten mit benutzerdefinierten Nachrichtenklassen vom standardmäßigen IPM unterscheiden. Hinweis Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="b7c97-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="b7c97-106">Benutzerdefinierte Nachrichtenklassen entsprechen Formular Servern, und Formularserver stellen Symbole bereit, die sich selbst darstellen.</span><span class="sxs-lookup"><span data-stu-id="b7c97-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="b7c97-107">Sie können diese Symbole in der Liste der Nachrichten anzeigen, um die Benutzer für die Nachrichtenklasse der einzelnen Nachrichten zu benachrichtigen, bevor der Benutzer die Nachricht öffnet.</span><span class="sxs-lookup"><span data-stu-id="b7c97-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="b7c97-108">In der Regel ist das Symbol in der **PR_MINI_ICON** ([pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaft des Formulars diejenige, die in der Liste der Nachrichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7c97-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="b7c97-109">Formulare verfügen außerdem über eine **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md))-Eigenschaft, die angezeigt werden kann, wenn das Formular in einem Eigenschaftenfenster minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="b7c97-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="b7c97-110">**So rufen Sie ein Symbol für eine Nachrichtenklasse ab, ohne den Formularserver für diese Nachrichtenklasse zu aktivieren**</span><span class="sxs-lookup"><span data-stu-id="b7c97-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="b7c97-111">Rufen Sie die [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode auf, um einen Zeiger auf eine [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7c97-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="b7c97-112">Rufen Sie die [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) -Methode auf, um einen Zeiger auf eine [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7c97-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="b7c97-113">Rufen Sie die [IMAPIFormInfo:: MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) -Methode auf, um ein Symbol-Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7c97-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="b7c97-114">Das Symbol kann dann mit standardmäßigen Win32-APIs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b7c97-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b7c97-115">Sobald Sie das Symbol für eine Nachrichtenklasse haben, sollten Sie das Symbol Zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="b7c97-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="b7c97-116">Nicht zwischenspeichernde Symbole haben gravierende Auswirkungen auf die Leistung von Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="b7c97-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="b7c97-117">Achten Sie beim Zwischenspeichern von Symbolen auf die Beziehungen zwischen Nachrichtenklassen und ihren Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="b7c97-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="b7c97-118">Wenn beispielsweise die IPM. Note. Meeting. Cancel-Nachrichtenklasse wird wieder in IPM aufgelöst. Beachten Sie, dass alle Unterklassen von IPM. Hinweis sollte das Symbol für IPM verwenden. Hinweis.</span><span class="sxs-lookup"><span data-stu-id="b7c97-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

