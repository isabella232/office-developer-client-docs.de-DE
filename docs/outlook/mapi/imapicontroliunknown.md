---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 80acb1a1e4663a68efc4692ab67ec27bc369f4b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566516"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="18ed3-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18ed3-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="18ed3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18ed3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18ed3-105">Aktiviert und ein Button-Steuerelement deaktiviert und führt Aufgaben aus, wenn ein Benutzer von einer Clientanwendung aktivierte Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="18ed3-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="18ed3-106">Dienstanbieter implementieren Control-Objekte zum Erstellen von benutzerdefinierter Schaltflächen auf Dialogfelder wie Konfiguration Property Sheets, die mithilfe der Anzeige Tabellen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="18ed3-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="18ed3-107">Weitere Informationen zum Arbeiten mit Tabellen anzeigen und Objekte zu steuern finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="18ed3-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18ed3-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="18ed3-108">Header file:</span></span>  <br/> |<span data-ttu-id="18ed3-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18ed3-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="18ed3-110">Verfügbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="18ed3-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="18ed3-111">Control-Objekte</span><span class="sxs-lookup"><span data-stu-id="18ed3-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="18ed3-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="18ed3-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="18ed3-113">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="18ed3-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="18ed3-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="18ed3-114">Called by:</span></span>  <br/> |<span data-ttu-id="18ed3-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="18ed3-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="18ed3-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="18ed3-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="18ed3-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="18ed3-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="18ed3-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="18ed3-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="18ed3-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="18ed3-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="18ed3-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="18ed3-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="18ed3-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="18ed3-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="18ed3-122">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Schaltfläche-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="18ed3-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="18ed3-123">Activate</span><span class="sxs-lookup"><span data-stu-id="18ed3-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="18ed3-124">Führt eine Aufgabe wie etwa Anzeigen eines Dialogfelds oder einen programmgesteuerten Vorgang starten, wenn Benutzer eine Clientanwendung das Button-Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="18ed3-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="18ed3-125">GetState</span><span class="sxs-lookup"><span data-stu-id="18ed3-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="18ed3-126">Ruft einen Wert, der angibt, ob das Schaltflächensteuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="18ed3-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18ed3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ed3-127">See also</span></span>



[<span data-ttu-id="18ed3-128">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="18ed3-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

