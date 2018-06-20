---
title: Formular Speicher
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a99ef76e63e634c661bf82bdab10b86c843e0df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791726"
---
# <a name="form-storage"></a><span data-ttu-id="69b48-103">Formular Speicher</span><span class="sxs-lookup"><span data-stu-id="69b48-103">Form storage</span></span>

<span data-ttu-id="69b48-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69b48-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69b48-105">Obwohl es nicht erforderlich ist, wissen Sie alle Details der wie Formulare physisch gespeichert sind, ist es sinnvoll, nur einige der wichtigsten Konzepte verstehen.</span><span class="sxs-lookup"><span data-stu-id="69b48-105">Although it is not necessary to know all the details of how forms are physically stored, it is useful to understand a few of the main concepts.</span></span> <span data-ttu-id="69b48-106">Bevor Sie die drei Typen von Formularbibliotheken mithilfe der Standard-Formular-Manager unterstützt beschreiben, bietet in diesem Thema daher eine Übersicht über wie Formulare gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="69b48-106">Therefore, before describing the three types of form libraries supported by the default form manager, this topic gives an overview of how forms are stored.</span></span>
  
<span data-ttu-id="69b48-107">Formulardefinitionen können in Ordnern in eine oder mehrere MAPI-Nachrichtenspeicher physisch gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="69b48-107">Form definitions can be physically stored within folders in one or more MAPI message stores.</span></span> <span data-ttu-id="69b48-108">Jedes MAPI-Ordners mit zwei Bereichen zum Speichern von Message-Objekten betrachtet werden kann: das standard-Webpart und das zugeordnete Teil.</span><span class="sxs-lookup"><span data-stu-id="69b48-108">Every MAPI folder can be thought of as having two areas for storing message objects: the standard part and the associated part.</span></span> <span data-ttu-id="69b48-109">Der standard Teil des Ordners enthält die Nachrichten und Ordnern, die Benutzer zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="69b48-109">The standard part of the folder includes the messages and folders that users manipulate.</span></span>
  
<span data-ttu-id="69b48-110">Das zugeordnete Teil umfasst ausgeblendete Nachricht-Objekte, die dem Ordner, einschließlich Formulardefinitionen, Ansichten, Vorlagen, Antwortvorlagen usw. zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="69b48-110">The associated part includes hidden message objects that are associated with the folder, including form definitions, views, rule templates, reply templates, and so on.</span></span> <span data-ttu-id="69b48-111">Diese Alternative Teil die Ordner verknüpfte Inhaltstabelle wird aufgerufen, und der Satz von Nachrichten in der zugehörigen Inhaltstabelle genannt wird die Informationen Ordner verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="69b48-111">This alternate part is called the folder-associated contents table, and the set of messages in the associated contents table is referred to as the folder-associated information.</span></span> <span data-ttu-id="69b48-112">Die ausgeblendeten Nachrichten sind ein integraler Bestandteil des Ordners und werden zusammen mit den Standardordner Inhalt kopiert, wenn der Ordner kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="69b48-112">The hidden messages are an integral part of the folder and are copied along with the standard folder contents when the folder is copied.</span></span> <span data-ttu-id="69b48-113">Obwohl physisch als Nachrichten gespeichert, unterscheidet sich Informationen in einem Ordner zugeordnete Inhaltstabelle mehr Eigenschaften als sichtbare Nachrichten wie.</span><span class="sxs-lookup"><span data-stu-id="69b48-113">Although physically stored as messages, information in a folder's associated contents table behaves more like properties than like viewable messages.</span></span> <span data-ttu-id="69b48-114">Alle Folder-Objekt, das eine Inhaltstabelle zugeordneten unterstützt kann zum Speichern von benutzerdefinierten Formularen.</span><span class="sxs-lookup"><span data-stu-id="69b48-114">Any folder object that supports an associated contents table is capable of storing custom forms.</span></span> <span data-ttu-id="69b48-115">Die [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) -Methode kann den Inhalt standard oder den zugehörigen Inhalt des Ordners, abhängig vom Wert des Parameters für die Methode _Ulflags_ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="69b48-115">The [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method can return either the standard contents or the associated contents of the folder, depending on the value of the method's  _ulflags_ parameter.</span></span> 
  
<span data-ttu-id="69b48-116">Besteht aus eine Formularbibliothek Formulardefinitionen, die in einem Ordner zugeordnete Inhaltstabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="69b48-116">A form library consists of form definitions stored in a folder's associated contents table.</span></span> <span data-ttu-id="69b48-117">Die Formulardefinition enthält die Eigenschaften des Formulars, die Aktionen des Formulars unterstützt, und auch das Formular Server ausführbare Datei, die als eine oder mehrere e-Mail-Anlagen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="69b48-117">The form definition includes the form's properties, the actions the form supports, and even the form server executable file, which is stored as one or more message attachments.</span></span>
  
<span data-ttu-id="69b48-118">Darüber hinaus können Formulare in eine Datei oder einen Speicherort, der der Formular-Manager verwendeten unterstützt gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="69b48-118">Additionally, forms can be stored in any file or location that the form manager being used supports.</span></span> <span data-ttu-id="69b48-119">Der Standard-Formular-Manager speichert Formular Servern in MAPI-Ordnern, aber ein benutzerdefiniertes Formular-Manager konnte einen eigene Speicher für Formular-Servern implementieren.</span><span class="sxs-lookup"><span data-stu-id="69b48-119">The default form manager stores form servers in MAPI folders, but a custom form manager could implement its own storage for form servers.</span></span>
  
<span data-ttu-id="69b48-120">Ein Formular kann mehrere Benutzeroberflächen enthalten, die auf deren Nachrichtenklasse gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="69b48-120">A form can have multiple user interfaces that are bound to its message class.</span></span> <span data-ttu-id="69b48-121">Beispielsweise kann ein Formular separate verfassen- und Benutzeroberflächen haben.</span><span class="sxs-lookup"><span data-stu-id="69b48-121">For example, a form can have separate Compose and Read user interfaces.</span></span> <span data-ttu-id="69b48-122">Das Formular akzeptiert Pflege des Aufrufs der entsprechenden Benutzeroberfläche für verschiedene Benutzeranfragen, je nachdem, welches das Formular Verben angerufen wird.</span><span class="sxs-lookup"><span data-stu-id="69b48-122">The form takes care of invoking the proper user interface for different user requests, depending on which of the form's verbs is being called.</span></span> <span data-ttu-id="69b48-123">Angenommen, wenn Ihr Formular Server separaten Verfassen und Lesen von Benutzeroberflächen verfügt, die Benutzeroberfläche zum Verfassen kann geöffnet werden automatisch, wenn der Benutzer eine neue Nachricht der Nachrichtenklasse des Formulars erstellt und die Read-Benutzeroberfläche geöffnet werden automatisch bei der Benutzer öffnet eine vorhandene Nachricht der Nachrichtenklasse des Formulars.</span><span class="sxs-lookup"><span data-stu-id="69b48-123">For example, if your form server has separate composing and reading user interfaces, the Compose user interface can be opened automatically when the user creates a new message of the form's message class and the Read user interface can be opened automatically when the user opens an existing message of the form's message class.</span></span>
  
<span data-ttu-id="69b48-124">Die meisten der Informationen in einer Formulardefinition ist durch Aufrufen der [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) -Methode für ein Objekt **IMAPIFormInfo** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="69b48-124">Most of the information stored within a form definition is available by invoking the [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) method on an **IMAPIFormInfo** object.</span></span> <span data-ttu-id="69b48-125">Die Schnittstelle **IMAPIFormInfo** vereinfacht den Zugriff auf Informationen für das Formular durch Aufrufen der MAPI-Ordner und die Nachricht angewendet werden, um die Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="69b48-125">The **IMAPIFormInfo** interface simplifies access to form information by calling all the MAPI folder and message methods needed to retrieve the information.</span></span> <span data-ttu-id="69b48-126">Ein **IMAPIFormInfo** -Objekt kann durch Aufrufen der Methode [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="69b48-126">An **IMAPIFormInfo** object can be obtained by calling the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method.</span></span> 
  
<span data-ttu-id="69b48-127">Die drei Typen von Formularbibliotheken werden in den Themen [Lokalen Formularbibliotheken](local-form-libraries.md), [Ordner Formularbibliotheken](folder-form-libraries.md) und [Persönliche Formularbibliotheken](personal-form-libraries.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69b48-127">The three types of form libraries are described in the topics [Local Form Libraries](local-form-libraries.md), [Folder Form Libraries](folder-form-libraries.md) and [Personal Form Libraries](personal-form-libraries.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="69b48-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69b48-128">See also</span></span>

- [<span data-ttu-id="69b48-129">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="69b48-129">MAPI Forms</span></span>](mapi-forms.md)
