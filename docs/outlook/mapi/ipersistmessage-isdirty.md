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
ms.openlocfilehash: 0d2ae556f4dd98b5f6e274a21c608d4ea364d4ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576204"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="50f3c-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="50f3c-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="50f3c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50f3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50f3c-105">Überprüft das Formular, damit die Änderungen, die seit dem letzten Speichervorgang vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="50f3c-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="50f3c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50f3c-106">Parameters</span></span>

<span data-ttu-id="50f3c-107">Keine</span><span class="sxs-lookup"><span data-stu-id="50f3c-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="50f3c-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="50f3c-108">Return value</span></span>

<span data-ttu-id="50f3c-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="50f3c-109">S_OK</span></span> 
  
> <span data-ttu-id="50f3c-110">Das Formular wurde geändert, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="50f3c-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="50f3c-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="50f3c-111">S_FALSE</span></span> 
  
> <span data-ttu-id="50f3c-112">Das Formular hat keine Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="50f3c-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50f3c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50f3c-113">Remarks</span></span>

<span data-ttu-id="50f3c-114">Formular Viewer rufen Sie die **IPersistMessage::IsDirty** -Methode, um zu bestimmen, ob die Nachricht Daten vorliegen.</span><span class="sxs-lookup"><span data-stu-id="50f3c-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50f3c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50f3c-115">See also</span></span>



[<span data-ttu-id="50f3c-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50f3c-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

