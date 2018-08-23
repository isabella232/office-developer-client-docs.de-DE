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
ms.openlocfilehash: 7ac8026489b06031e07ab4b2978c9ece04063bb1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579144"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="d1694-103">Anzeigen von Formularsymbolen</span><span class="sxs-lookup"><span data-stu-id="d1694-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="d1694-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1694-105">Beim Anzeigen einer Liste von Nachrichten in einem Ordner ist es hilfreich, die Benutzer, wenn Sie von der standardmäßigen IPM Nachrichten mit benutzerdefinierten Nachrichtenklassen unterscheiden. Beachten Sie Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d1694-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="d1694-106">Benutzerdefinierte Nachrichtenklassen entsprechen den Formular-Servern und Formular Server bieten Symbole, um sich selbst darstellen.</span><span class="sxs-lookup"><span data-stu-id="d1694-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="d1694-107">Sie können diese Symbole in der Liste der Nachrichten an Benutzer zu jeder Nachricht Nachrichtenklasse anzeigen, bevor der Benutzer die Nachrichten öffnet.</span><span class="sxs-lookup"><span data-stu-id="d1694-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="d1694-108">Das Symbol in das Formular **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))-Eigenschaft ist in der Regel diejenige, die in der Liste der Nachrichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1694-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="d1694-109">Formulare enthalten auch eine **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md))-Eigenschaft, die angezeigt werden, wenn das Formular in einem Eigenschaftenfenster minimiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1694-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="d1694-110">**Um ein Symbol für eine Nachrichtenklasse zu erhalten, ohne Aktivieren der Formular-Servers für die Nachrichtenklasse**</span><span class="sxs-lookup"><span data-stu-id="d1694-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="d1694-111">Rufen Sie die [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) -Methode, um einen Zeiger auf eine [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d1694-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="d1694-112">Rufen Sie die [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) -Methode, um einen Zeiger auf eine [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d1694-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="d1694-113">Rufen Sie die [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) -Methode, um ein Symbolhandle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1694-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="d1694-114">Das Symbol kann mit standard Win32-APIs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d1694-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d1694-115">Nachdem Sie das Symbol für eine Nachrichtenklasse haben, stellen Sie bemüht, Symbol zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1694-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="d1694-116">Zwischenspeichern von Symbolen nicht schwerwiegend wirkt sich auf die Leistung von Clientanwendungen aus.</span><span class="sxs-lookup"><span data-stu-id="d1694-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="d1694-117">Beim Zwischenspeichern von Symbolen, achten Sie auf die Beziehungen zwischen Nachrichtenklassen und ihre Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="d1694-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="d1694-118">Angenommen, wenn die IPM. Note.Meeting.Cancel Nachrichtenklasse geschieht mit wieder auf IPM zu beheben. Beachten Sie, nicht angenommen wird, die alle Unterklassen IPM. Hinweis sollte das Symbol für IPM verwendet werden. Beachten Sie.</span><span class="sxs-lookup"><span data-stu-id="d1694-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

