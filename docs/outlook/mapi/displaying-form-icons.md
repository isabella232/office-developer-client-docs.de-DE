---
title: Anzeigen von Form von Symbolen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791563"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="d9f0a-103">Anzeigen von Form von Symbolen</span><span class="sxs-lookup"><span data-stu-id="d9f0a-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="d9f0a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9f0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9f0a-105">Beim Anzeigen einer Liste von Nachrichten in einem Ordner ist es hilfreich, die Benutzer, wenn Sie von der standardmäßigen IPM Nachrichten mit benutzerdefinierten Nachrichtenklassen unterscheiden. Beachten Sie Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="d9f0a-106">Benutzerdefinierte Nachrichtenklassen entsprechen den Formular-Servern und Formular Server bieten Symbole, um sich selbst darstellen.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="d9f0a-107">Sie können diese Symbole in der Liste der Nachrichten an Benutzer zu jeder Nachricht Nachrichtenklasse anzeigen, bevor der Benutzer die Nachrichten öffnet.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="d9f0a-108">Das Symbol in das Formular **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaft ist in der Regel diejenige, die in der Liste der Nachrichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="d9f0a-109">Formulare enthalten auch eine **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md))-Eigenschaft, die angezeigt werden, wenn das Formular in einem Eigenschaftenfenster minimiert ist.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="d9f0a-110">**Um ein Symbol für eine Nachrichtenklasse zu erhalten, ohne Aktivieren der Formular-Servers für die Nachrichtenklasse**</span><span class="sxs-lookup"><span data-stu-id="d9f0a-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="d9f0a-111">Rufen Sie die [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode, um einen Zeiger auf eine [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="d9f0a-112">Rufen Sie die [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) -Methode, um einen Zeiger auf eine [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="d9f0a-113">Rufen Sie die [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) -Methode, um ein Symbolhandle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="d9f0a-114">Das Symbol kann mit standard Win32-APIs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d9f0a-115">Nachdem Sie das Symbol für eine Nachrichtenklasse haben, stellen Sie bemüht, Symbol zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="d9f0a-116">Zwischenspeichern von Symbolen nicht schwerwiegend wirkt sich auf die Leistung von Clientanwendungen aus.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="d9f0a-117">Beim Zwischenspeichern von Symbolen, achten Sie auf die Beziehungen zwischen Nachrichtenklassen und ihre Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="d9f0a-118">Angenommen, wenn die IPM. Note.Meeting.Cancel Nachrichtenklasse geschieht mit wieder auf IPM zu beheben. Beachten Sie, nicht angenommen wird, die alle Unterklassen IPM. Hinweis sollte das Symbol für IPM verwendet werden. Beachten Sie.</span><span class="sxs-lookup"><span data-stu-id="d9f0a-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

