---
title: IPersistMessageIsDirty
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.IsDirty
api_type:
- COM
ms.assetid: 57f688db-3a1c-49ff-a15a-8508bda5de68
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91985d3dc8a7816c3da3215e505097c57c63e035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309611"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="3ec44-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="3ec44-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="3ec44-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec44-105">Überprüft das Formular auf Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3ec44-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="3ec44-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ec44-106">Parameters</span></span>

<span data-ttu-id="3ec44-107">Keine</span><span class="sxs-lookup"><span data-stu-id="3ec44-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="3ec44-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ec44-108">Return value</span></span>

<span data-ttu-id="3ec44-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ec44-109">S_OK</span></span> 
  
> <span data-ttu-id="3ec44-110">Das Formular enthält Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3ec44-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="3ec44-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3ec44-111">S_FALSE</span></span> 
  
> <span data-ttu-id="3ec44-112">Das Formular verfügt nicht über Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3ec44-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ec44-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ec44-113">Remarks</span></span>

<span data-ttu-id="3ec44-114">Formular Betrachter rufen die **IPersistMessage:: IsDirty** -Methode auf, um zu bestimmen, ob die Nachricht nicht gespeicherte Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3ec44-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ec44-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ec44-115">See also</span></span>



[<span data-ttu-id="3ec44-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ec44-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

