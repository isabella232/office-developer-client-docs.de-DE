---
title: Status „Nicht initialisiert“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578248"
---
# <a name="uninitialized-state"></a><span data-ttu-id="f1481-103">Status „Nicht initialisiert“</span><span class="sxs-lookup"><span data-stu-id="f1481-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="f1481-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1481-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1481-105">Initialisierte Zustand ist der Anfangszustand-Formular, die Objekte in werden sollen, wenn sie zuerst erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f1481-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="f1481-106">Formular-Objekte werden mit Meldungsdaten initialisiert, wenn eine Clientanwendung für das Form-Objekt die [IPersistMessage::InitNew](ipersistmessage-initnew.md) oder [IPersistMessage::Load](ipersistmessage-load.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="f1481-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="f1481-107">In der folgenden Tabelle werden die zulässigen Übergänge aus dem Status Unitialized beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1481-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="f1481-108">**IPersistMessage-Methode**</span><span class="sxs-lookup"><span data-stu-id="f1481-108">**IPersistMessage method**</span></span>|<span data-ttu-id="f1481-109">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="f1481-109">**Action**</span></span>|<span data-ttu-id="f1481-110">**Neue Zustand**</span><span class="sxs-lookup"><span data-stu-id="f1481-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1481-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="f1481-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="f1481-112">Laden Sie das Form-Objekt mit Standarddaten.</span><span class="sxs-lookup"><span data-stu-id="f1481-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="f1481-113">Normal</span><span class="sxs-lookup"><span data-stu-id="f1481-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="f1481-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="f1481-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="f1481-115">Laden Sie das Form-Objekt mit Daten aus der Zielnachricht.</span><span class="sxs-lookup"><span data-stu-id="f1481-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="f1481-116">Standard</span><span class="sxs-lookup"><span data-stu-id="f1481-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="f1481-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="f1481-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="f1481-118">Zurückgeben von Erfolg, oder legen Sie den letzten Fehler auf und E_UNEXPECTED zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f1481-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="f1481-119">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="f1481-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="f1481-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f1481-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="f1481-121">Geben Sie den letzten Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f1481-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="f1481-122">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="f1481-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="f1481-123">Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) Methoden oder Methoden aus anderen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f1481-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="f1481-124">Legen Sie den letzten Fehler auf und zurückgeben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="f1481-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="f1481-125">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="f1481-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1481-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1481-126">See also</span></span>



[<span data-ttu-id="f1481-127">Status „Normal“</span><span class="sxs-lookup"><span data-stu-id="f1481-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="f1481-128">Formularstatus</span><span class="sxs-lookup"><span data-stu-id="f1481-128">Form States</span></span>](form-states.md)

