---
title: Implementieren von Standard mäßigen Formular Verben
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
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="58d24-103">Implementieren von Standard mäßigen Formular Verben</span><span class="sxs-lookup"><span data-stu-id="58d24-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="58d24-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58d24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58d24-105">MAPI definiert eine Reihe von Standardverben oder Aktionen, die ausgeführt werden, wenn ein Benutzer eine Menüauswahl vornimmt oder auf eine Schaltfläche klickt, die von allen Formular Betrachtern unterstützt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="58d24-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="58d24-106">Jedem Verb ist eine Konstante zugeordnet, die in der EXCHFORM definiert ist. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="58d24-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="58d24-107">In der folgenden Tabelle sind die standardmäßigen Verben und die zugehörigen Konstanten aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="58d24-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="58d24-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="58d24-108">**Verb**</span></span>|<span data-ttu-id="58d24-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="58d24-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58d24-110">Öffnen</span><span class="sxs-lookup"><span data-stu-id="58d24-110">Open</span></span>  <br/> |<span data-ttu-id="58d24-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="58d24-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="58d24-112">Antworten</span><span class="sxs-lookup"><span data-stu-id="58d24-112">Reply</span></span>  <br/> |<span data-ttu-id="58d24-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="58d24-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="58d24-114">Allen antworten</span><span class="sxs-lookup"><span data-stu-id="58d24-114">Reply to All</span></span>  <br/> |<span data-ttu-id="58d24-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="58d24-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="58d24-116">Weiterleiten</span><span class="sxs-lookup"><span data-stu-id="58d24-116">Forward</span></span>  <br/> |<span data-ttu-id="58d24-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="58d24-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="58d24-118">Print</span><span class="sxs-lookup"><span data-stu-id="58d24-118">Print</span></span>  <br/> |<span data-ttu-id="58d24-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="58d24-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="58d24-120">Speichern unter</span><span class="sxs-lookup"><span data-stu-id="58d24-120">Save As</span></span>  <br/> |<span data-ttu-id="58d24-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="58d24-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="58d24-122">In Ordner antworten</span><span class="sxs-lookup"><span data-stu-id="58d24-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="58d24-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="58d24-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="58d24-124">Wenn ein Benutzer ein Verb auswählt, übergibt seine Konstante in einem Aufruf an die [IMAPIForm::D overb](imapiform-doverb.md) -Methode des Formulars, um die entsprechende Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="58d24-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="58d24-125">Zusätzlich zum Zugreifen auf Verben über den Formular Betrachter können Benutzer manchmal direkt über das Formular auf Verben zugreifen.</span><span class="sxs-lookup"><span data-stu-id="58d24-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="58d24-126">Einige Formularobjekte ermöglichen es dem Benutzer beispielsweise, das **Druck** -Verb aufzurufen, indem Sie mit der rechten Maustaste auf das Formular klicken und im kontextabhängigen Menü **Drucken** auswählen.</span><span class="sxs-lookup"><span data-stu-id="58d24-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

