---
title: Anzeigen von Tabellensteuerelementen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 37f6cd0320894d500416672c3dd0d90ee3324b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422691"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="e788d-103">Anzeigen von Tabellensteuerelementen</span><span class="sxs-lookup"><span data-stu-id="e788d-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="e788d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e788d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e788d-105">Es gibt viele verschiedene Typen von Steuerelementen, die für MAPI nicht eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="e788d-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="e788d-106">MAPI definiert jedoch eigene Strukturen, die in Verbindung mit [BuildDisplayTable](builddisplaytable.md) verwendet werden, um die eindeutigen Datensätze zu beschreiben, die mit den einzelnen Steuerelementen verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="e788d-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="e788d-107">In der folgenden Tabelle sind die Strukturen aufgelistet, in denen die einzelnen Steuerelementtypen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e788d-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="e788d-108">**Steuerelementstruktur**</span><span class="sxs-lookup"><span data-stu-id="e788d-108">**Control structure**</span></span>|<span data-ttu-id="e788d-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e788d-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e788d-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="e788d-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="e788d-111">Beschreibt ein Schaltflächen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="e788d-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="e788d-113">Beschreibt ein Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="e788d-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="e788d-115">Beschreibt ein Kombinationsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="e788d-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="e788d-117">Beschreibt ein Dropdown-Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="e788d-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="e788d-119">Beschreibt ein Bearbeitungssteuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="e788d-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="e788d-121">Beschreibt ein Gruppenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="e788d-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="e788d-123">Beschreibt ein Label-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="e788d-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="e788d-125">Beschreibt ein Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="e788d-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="e788d-127">Beschreibt ein Dropdown-Listenfeld-Steuerelement mit mehreren Werten.</span><span class="sxs-lookup"><span data-stu-id="e788d-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="e788d-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="e788d-129">Beschreibt ein Listenfeld-Steuerelement mit mehreren Werten.</span><span class="sxs-lookup"><span data-stu-id="e788d-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="e788d-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="e788d-131">Beschreibt ein Seitensteuerelement mit Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="e788d-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="e788d-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="e788d-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="e788d-133">Beschreibt ein Optionsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="e788d-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e788d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e788d-134">See also</span></span>



[<span data-ttu-id="e788d-135">Anzeigen der Tabellen Implementierung</span><span class="sxs-lookup"><span data-stu-id="e788d-135">Display Table Implementation</span></span>](display-table-implementation.md)

