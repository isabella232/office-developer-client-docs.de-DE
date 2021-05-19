---
title: Nicht initialisierter Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425561"
---
# <a name="uninitialized-state"></a><span data-ttu-id="22e00-103">Nicht initialisierter Status</span><span class="sxs-lookup"><span data-stu-id="22e00-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="22e00-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22e00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22e00-105">Der Status "Nicht initialisiert" ist der Anfangszustand, in dem sich Formularobjekte befinden sollten, wenn sie zum ersten Mal erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="22e00-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="22e00-106">Formularobjekte werden mit Nachrichtendaten initialisiert, wenn eine Clientanwendung die [IPersistMessage::InitNew-](ipersistmessage-initnew.md) oder [IPersistMessage::Load-Methode](ipersistmessage-load.md) für das Formularobjekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="22e00-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="22e00-107">In der folgenden Tabelle werden zulässige Übergänge vom Unitialized-Zustand beschrieben.</span><span class="sxs-lookup"><span data-stu-id="22e00-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="22e00-108">**IPersistMessage-Methode**</span><span class="sxs-lookup"><span data-stu-id="22e00-108">**IPersistMessage method**</span></span>|<span data-ttu-id="22e00-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="22e00-109">**Action**</span></span>|<span data-ttu-id="22e00-110">**Neuer Status**</span><span class="sxs-lookup"><span data-stu-id="22e00-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="22e00-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="22e00-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="22e00-112">Laden Sie das Formularobjekt mit Standarddaten.</span><span class="sxs-lookup"><span data-stu-id="22e00-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="22e00-113">Normal</span><span class="sxs-lookup"><span data-stu-id="22e00-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="22e00-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="22e00-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="22e00-115">Laden Sie das Formularobjekt mit Daten aus der Zielnachricht.</span><span class="sxs-lookup"><span data-stu-id="22e00-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="22e00-116">Standard</span><span class="sxs-lookup"><span data-stu-id="22e00-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="22e00-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="22e00-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="22e00-118">Zurückgeben des Erfolgs oder Festlegen des letzten Fehlers auf und Zurückgeben E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="22e00-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="22e00-119">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="22e00-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="22e00-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="22e00-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="22e00-121">Gibt den letzten Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="22e00-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="22e00-122">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="22e00-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="22e00-123">Andere [IPersistMessage : IUnknown-Methoden](ipersistmessageiunknown.md) oder -Methoden aus anderen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="22e00-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="22e00-124">Legen Sie den letzten Fehler auf und geben E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="22e00-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="22e00-125">Nicht initialisiert</span><span class="sxs-lookup"><span data-stu-id="22e00-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22e00-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22e00-126">See also</span></span>



[<span data-ttu-id="22e00-127">Normalzustand</span><span class="sxs-lookup"><span data-stu-id="22e00-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="22e00-128">Formularzustände</span><span class="sxs-lookup"><span data-stu-id="22e00-128">Form States</span></span>](form-states.md)

