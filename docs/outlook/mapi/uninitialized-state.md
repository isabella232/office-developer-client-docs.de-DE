---
title: Nicht initialisierter Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360501"
---
# <a name="uninitialized-state"></a><span data-ttu-id="1ed03-103">Nicht initialisierter Status</span><span class="sxs-lookup"><span data-stu-id="1ed03-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="1ed03-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ed03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ed03-105">Der nicht initialisierte Status ist der anfängliche Zustand, in dem Formularobjekte bei der ersten Erstellung vorliegen sollen.</span><span class="sxs-lookup"><span data-stu-id="1ed03-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="1ed03-106">Formularobjekte werden mit Nachrichtendaten initialisiert, wenn eine Clientanwendung die [IPersistMessage:: InitNew](ipersistmessage-initnew.md) -oder [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode für das Form-Objekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="1ed03-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="1ed03-107">In der folgenden Tabelle werden zulässige Übergänge vom initialisierten-Status beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ed03-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="1ed03-108">**IPersistMessage-Methode**</span><span class="sxs-lookup"><span data-stu-id="1ed03-108">**IPersistMessage method**</span></span>|<span data-ttu-id="1ed03-109">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="1ed03-109">**Action**</span></span>|<span data-ttu-id="1ed03-110">**Neuer Status**</span><span class="sxs-lookup"><span data-stu-id="1ed03-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1ed03-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="1ed03-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="1ed03-112">Laden Sie das Form-Objekt mit Standarddaten.</span><span class="sxs-lookup"><span data-stu-id="1ed03-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="1ed03-113">Normal</span><span class="sxs-lookup"><span data-stu-id="1ed03-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="1ed03-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="1ed03-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="1ed03-115">Laden Sie das Form-Objekt mit Daten aus der Zielnachricht.</span><span class="sxs-lookup"><span data-stu-id="1ed03-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="1ed03-116">Normal</span><span class="sxs-lookup"><span data-stu-id="1ed03-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="1ed03-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="1ed03-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="1ed03-118">Zurückgeben des Erfolgs oder Festlegen des letzten Fehlers auf und Zurückgeben von E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="1ed03-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="1ed03-119">Initialisierten</span><span class="sxs-lookup"><span data-stu-id="1ed03-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="1ed03-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1ed03-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="1ed03-121">Zurückgeben des letzten Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1ed03-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="1ed03-122">Initialisierten</span><span class="sxs-lookup"><span data-stu-id="1ed03-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="1ed03-123">Andere [IPersistMessage: IUnknown](ipersistmessageiunknown.md) -Methoden oder Methoden von anderen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ed03-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="1ed03-124">Legen Sie den letzten Fehler an und geben Sie E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="1ed03-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="1ed03-125">Initialisierten</span><span class="sxs-lookup"><span data-stu-id="1ed03-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ed03-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ed03-126">See also</span></span>



[<span data-ttu-id="1ed03-127">Normaler Status</span><span class="sxs-lookup"><span data-stu-id="1ed03-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="1ed03-128">Formular Status</span><span class="sxs-lookup"><span data-stu-id="1ed03-128">Form States</span></span>](form-states.md)

