---
title: Implementieren von standardmäßigen Formularverben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792577"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="952a2-103">Implementieren von standardmäßigen Formularverben</span><span class="sxs-lookup"><span data-stu-id="952a2-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="952a2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="952a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="952a2-105">MAPI definiert eine Reihe von standardmäßigen Verben oder Aktionen ausgeführt, wenn ein Benutzer eine Menüauswahl im trifft oder auf eine Schaltfläche, die alle Formular-Viewer unterstützen soll.</span><span class="sxs-lookup"><span data-stu-id="952a2-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="952a2-106">Jedes Verb hat, eine Konstante, die für die Identifikation in der EXCHFORM definierten zugeordnet wird. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="952a2-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="952a2-107">Die folgende Tabelle enthält die Standardformular Verben und deren zugeordneten Konstanten:</span><span class="sxs-lookup"><span data-stu-id="952a2-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="952a2-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="952a2-108">**Verb**</span></span>|<span data-ttu-id="952a2-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="952a2-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="952a2-110">Öffnen</span><span class="sxs-lookup"><span data-stu-id="952a2-110">Open</span></span>  <br/> |<span data-ttu-id="952a2-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="952a2-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="952a2-112">Antworten</span><span class="sxs-lookup"><span data-stu-id="952a2-112">Reply</span></span>  <br/> |<span data-ttu-id="952a2-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="952a2-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="952a2-114">Allen antworten</span><span class="sxs-lookup"><span data-stu-id="952a2-114">Reply to All</span></span>  <br/> |<span data-ttu-id="952a2-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="952a2-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="952a2-116">Forward</span><span class="sxs-lookup"><span data-stu-id="952a2-116">Forward</span></span>  <br/> |<span data-ttu-id="952a2-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="952a2-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="952a2-118">Drucken</span><span class="sxs-lookup"><span data-stu-id="952a2-118">Print</span></span>  <br/> |<span data-ttu-id="952a2-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="952a2-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="952a2-120">Speichern als</span><span class="sxs-lookup"><span data-stu-id="952a2-120">Save As</span></span>  <br/> |<span data-ttu-id="952a2-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="952a2-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="952a2-122">In Ordner antworten</span><span class="sxs-lookup"><span data-stu-id="952a2-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="952a2-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="952a2-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="952a2-124">Wenn ein Benutzer ein Verb auswählt, übergeben Sie die Konstante in einen Anruf an das Formular [IMAPIForm::DoVerb](imapiform-doverb.md) -Methode zum Ausführen der entsprechenden Aktion.</span><span class="sxs-lookup"><span data-stu-id="952a2-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="952a2-125">Benutzer können über Ihr Formular Viewer auf Verben zugreifen, Verben manchmal direkt aus dem Formular zugreifen.</span><span class="sxs-lookup"><span data-stu-id="952a2-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="952a2-126">Beispielsweise Benutzer einige Formularobjekte sollen das Verb **Drucken** aufrufen, indem Sie mit der rechten Maustaste auf das Formular, und wählen Sie **Drucken** aus einem Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="952a2-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

