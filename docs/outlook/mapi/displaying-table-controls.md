---
title: Anzeigen von Table-Steuerelementen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 11b3279582c4cfb0d2c2249c6f4eddd7f0260b49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791571"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="0e805-103">Anzeigen von Table-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0e805-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="0e805-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e805-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e805-105">Es gibt viele verschiedene Typen von Steuerelementen, keine eindeutige MAPI.</span><span class="sxs-lookup"><span data-stu-id="0e805-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="0e805-106">MAPI definiert eine eigene Strukturen, die verwendet werden jedoch in Verbindung mit [BuildDisplayTable](builddisplaytable.md) zum Beschreiben des eindeutigen Satz von Daten, die an jedes Steuerelement beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="0e805-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="0e805-107">Die folgende Tabelle enthält die Strukturen, die jede Art von Steuerelement zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0e805-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="0e805-108">**Kontrollstruktur**</span><span class="sxs-lookup"><span data-stu-id="0e805-108">**Control structure**</span></span>|<span data-ttu-id="0e805-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0e805-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e805-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="0e805-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="0e805-111">Beschreibt ein Button-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="0e805-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="0e805-113">Beschreibt ein Kontrollkästchen-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="0e805-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="0e805-115">Beschreibt ein Kombinationsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="0e805-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="0e805-117">Beschreibt ein Dropdown-Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="0e805-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="0e805-119">Beschreibt ein Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="0e805-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="0e805-121">Beschreibt ein Gruppenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="0e805-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="0e805-123">Beschreibt ein Label-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="0e805-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="0e805-125">Beschreibt ein Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="0e805-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="0e805-127">Beschreibt eine mehrwertige Dropdown-Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="0e805-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="0e805-129">Beschreibt eine mehrwertige Listenfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="0e805-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="0e805-131">Beschreibt eine mit Registerkarten-Seitensteuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="0e805-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="0e805-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="0e805-133">Beschreibt ein Optionsfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0e805-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e805-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e805-134">See also</span></span>



[<span data-ttu-id="0e805-135">Implementierung der Anzeige-Tabelle</span><span class="sxs-lookup"><span data-stu-id="0e805-135">Display Table Implementation</span></span>](display-table-implementation.md)

