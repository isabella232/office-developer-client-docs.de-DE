---
title: Implementieren von Standardformularverben
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426121"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="a5910-103">Implementieren von Standardformularverben</span><span class="sxs-lookup"><span data-stu-id="a5910-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="a5910-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5910-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5910-105">MAPI definiert eine Reihe von Standardverben oder Aktionen, die von allen Formularbetrachtern unterstützt werden sollen, wenn ein Benutzer eine Menüauswahl vor nimmt oder auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="a5910-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="a5910-106">Jedem Verb ist eine Konstante zur Identifikation zugeordnet, die in EXCHFORM definiert ist. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="a5910-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="a5910-107">In der folgenden Tabelle sind die Standardformularverben und die zugehörigen Konstanten aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="a5910-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="a5910-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="a5910-108">**Verb**</span></span>|<span data-ttu-id="a5910-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a5910-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a5910-110">Öffnen</span><span class="sxs-lookup"><span data-stu-id="a5910-110">Open</span></span>  <br/> |<span data-ttu-id="a5910-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="a5910-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="a5910-112">Reply</span><span class="sxs-lookup"><span data-stu-id="a5910-112">Reply</span></span>  <br/> |<span data-ttu-id="a5910-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="a5910-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="a5910-114">Allen antworten</span><span class="sxs-lookup"><span data-stu-id="a5910-114">Reply to All</span></span>  <br/> |<span data-ttu-id="a5910-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="a5910-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="a5910-116">Forward</span><span class="sxs-lookup"><span data-stu-id="a5910-116">Forward</span></span>  <br/> |<span data-ttu-id="a5910-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="a5910-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="a5910-118">Drucken</span><span class="sxs-lookup"><span data-stu-id="a5910-118">Print</span></span>  <br/> |<span data-ttu-id="a5910-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="a5910-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="a5910-120">Speichern unter</span><span class="sxs-lookup"><span data-stu-id="a5910-120">Save As</span></span>  <br/> |<span data-ttu-id="a5910-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="a5910-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="a5910-122">In Ordner antworten</span><span class="sxs-lookup"><span data-stu-id="a5910-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="a5910-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="a5910-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="a5910-124">Wenn ein Benutzer ein Verb aus wählt, übergeben Sie seine Konstante in einem Aufruf an die [IMAPIForm::D oVerb-Methode](imapiform-doverb.md) des Formulars, um die entsprechende Aktion durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a5910-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="a5910-125">Neben dem Zugriff auf Verben über die Formularanzeige können Benutzer manchmal direkt über das Formular auf Verben zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a5910-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="a5910-126">Bei einigen Formularobjekten kann der Benutzer beispielsweise das **Verb Print** aufrufen, indem er mit der rechten Maustaste auf das Formular klickt und **in** einem kontextbezogenen Menü Drucken wählt.</span><span class="sxs-lookup"><span data-stu-id="a5910-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

