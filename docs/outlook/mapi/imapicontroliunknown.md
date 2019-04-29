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
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414039"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="817df-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="817df-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="817df-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="817df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="817df-105">Aktiviert und deaktiviert ein Schaltflächen-Steuerelement und führt Aufgaben aus, wenn ein Benutzer einer Clientanwendung auf das aktivierte Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="817df-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="817df-106">Dienstanbieter implementieren Steuerelemente zum Erstellen benutzerdefinierter Schaltflächen in Dialogfeldern, wie beispielsweise Konfigurationseigenschaften Blätter, die mithilfe von Anzeige Tabellen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="817df-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="817df-107">Weitere Informationen zum Arbeiten mit Anzeige Tabellen und Steuerelementobjekten finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="817df-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="817df-108">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="817df-108">Header file:</span></span>  <br/> |<span data-ttu-id="817df-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="817df-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="817df-110">Verf�gbar gemacht von:</span><span class="sxs-lookup"><span data-stu-id="817df-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="817df-111">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="817df-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="817df-112">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="817df-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="817df-113">Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="817df-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="817df-114">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="817df-114">Called by:</span></span>  <br/> |<span data-ttu-id="817df-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="817df-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="817df-116">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="817df-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="817df-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="817df-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="817df-118">Zeigertyp:</span><span class="sxs-lookup"><span data-stu-id="817df-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="817df-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="817df-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="817df-120">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="817df-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="817df-121">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="817df-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="817df-122">Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Fehler der Schaltflächensteuerung enthält.</span><span class="sxs-lookup"><span data-stu-id="817df-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="817df-123">Activate</span><span class="sxs-lookup"><span data-stu-id="817df-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="817df-124">Führt eine Aufgabe wie das Anzeigen eines Dialogfelds oder das Starten eines programmgesteuerten Vorgangs aus, wenn ein Benutzer der Clientanwendung auf das Schaltflächen-Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="817df-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="817df-125">GetState</span><span class="sxs-lookup"><span data-stu-id="817df-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="817df-126">Ruft einen Wert ab, der angibt, ob das Schaltflächen-Steuerelement aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="817df-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="817df-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="817df-127">See also</span></span>



[<span data-ttu-id="817df-128">MAPI-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="817df-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

