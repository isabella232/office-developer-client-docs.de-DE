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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792076"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="b4438-103">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4438-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="b4438-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4438-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4438-105">Aktiviert und ein Button-Steuerelement deaktiviert und führt Aufgaben aus, wenn ein Benutzer von einer Clientanwendung aktivierte Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="b4438-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="b4438-106">Dienstanbieter implementieren Control-Objekte zum Erstellen von benutzerdefinierter Schaltflächen auf Dialogfelder wie Konfiguration Property Sheets, die mithilfe der Anzeige Tabellen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b4438-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="b4438-107">Weitere Informationen zum Arbeiten mit Tabellen anzeigen und Objekte zu steuern finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b4438-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4438-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b4438-108">Header file:</span></span>  <br/> |<span data-ttu-id="b4438-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4438-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b4438-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="b4438-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="b4438-111">Control-Objekte</span><span class="sxs-lookup"><span data-stu-id="b4438-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="b4438-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b4438-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b4438-113">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b4438-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="b4438-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b4438-114">Called by:</span></span>  <br/> |<span data-ttu-id="b4438-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="b4438-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="b4438-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b4438-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b4438-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="b4438-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="b4438-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="b4438-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="b4438-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="b4438-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b4438-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b4438-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b4438-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b4438-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="b4438-122">Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Schaltfläche-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="b4438-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="b4438-123">Activate</span><span class="sxs-lookup"><span data-stu-id="b4438-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="b4438-124">Führt eine Aufgabe wie etwa Anzeigen eines Dialogfelds oder einen programmgesteuerten Vorgang starten, wenn Benutzer eine Clientanwendung das Button-Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="b4438-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="b4438-125">GetState</span><span class="sxs-lookup"><span data-stu-id="b4438-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="b4438-126">Ruft einen Wert, der angibt, ob das Schaltflächensteuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b4438-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4438-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4438-127">See also</span></span>



[<span data-ttu-id="b4438-128">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b4438-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

