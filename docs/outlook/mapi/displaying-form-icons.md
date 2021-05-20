---
title: Anzeigen von Formularsymbolen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438631"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="92d56-103">Anzeigen von Formularsymbolen</span><span class="sxs-lookup"><span data-stu-id="92d56-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="92d56-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92d56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92d56-105">Beim Anzeigen einer Liste von Nachrichten in einem Ordner ist es für Ihre Benutzer hilfreich, wenn Sie Nachrichten mit benutzerdefinierten Nachrichtenklassen vom standardmäßigen IPM unterscheiden. Notieren Sie sich Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="92d56-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="92d56-106">Benutzerdefinierte Nachrichtenklassen entsprechen Formularservern, und Formularserver stellen Symbole für sich selbst zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="92d56-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="92d56-107">Sie können diese Symbole in der Liste der Nachrichten anzeigen, um Benutzer vor dem Öffnen der Nachrichten vor der Nachrichtenklasse der einzelnen Nachrichten zu warnen.</span><span class="sxs-lookup"><span data-stu-id="92d56-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="92d56-108">In der Regel ist das Symbol in der **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaft das Symbol, das in der Liste der Nachrichten angezeigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="92d56-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="92d56-109">Formulare verfügen auch **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) -Eigenschaft, die angezeigt werden kann, wenn das Formular in einem Eigenschaftenblatt minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="92d56-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="92d56-110">**So erhalten Sie ein Symbol für eine Nachrichtenklasse, ohne den Formularserver für diese Nachrichtenklasse zu aktivieren**</span><span class="sxs-lookup"><span data-stu-id="92d56-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="92d56-111">Rufen Sie [die IMAPIFormMgr::OpenFormContainer-Methode](imapiformmgr-openformcontainer.md) auf, um einen Zeiger auf eine [IMAPIFormContainer : IUnknown-Schnittstelle zu](imapiformcontaineriunknown.md) erhalten.</span><span class="sxs-lookup"><span data-stu-id="92d56-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="92d56-112">Rufen Sie [die IMAPIFormContainer::ResolveMessageClass-Methode](imapiformcontainer-resolvemessageclass.md) auf, um einen Zeiger auf eine [IMAPIFormInfo : IMAPIProp-Schnittstelle zu](imapiforminfoimapiprop.md) erhalten.</span><span class="sxs-lookup"><span data-stu-id="92d56-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="92d56-113">Rufen Sie [die IMAPIFormInfo::MakeIconFromBinary-Methode](imapiforminfo-makeiconfrombinary.md) auf, um ein Symbolhandle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="92d56-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="92d56-114">Das Symbol kann dann mit standardmäßigen Win32-APIs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="92d56-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="92d56-115">Sobald Sie über das Symbol für eine Nachrichtenklasse verfügen, müssen Sie alles tun, um dieses Symbol zwischenspeichern.</span><span class="sxs-lookup"><span data-stu-id="92d56-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="92d56-116">Das Zwischenspeichern von Symbolen hat schwerwiegende Auswirkungen auf die Leistung von Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="92d56-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="92d56-117">Achten Sie beim Zwischenspeichern von Symbolen auf die Beziehungen zwischen Nachrichtenklassen und ihren Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="92d56-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="92d56-118">Beispiel: Wenn das IPM. Note.Meeting.Cancel-Nachrichtenklasse wird wieder in IPM aufgelöst. Beachten Sie, dass nicht alle Unterklassen von IPM angenommen werden. Hinweis sollte das Symbol für IPM verwenden. Hinweis.</span><span class="sxs-lookup"><span data-stu-id="92d56-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

