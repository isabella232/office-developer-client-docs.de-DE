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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e748427b39418a80cae88e98b4aa7eef6df24393
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792743"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="0767b-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="0767b-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="0767b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0767b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0767b-105">Überprüft das Formular, damit die Änderungen, die seit dem letzten Speichervorgang vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="0767b-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="0767b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0767b-106">Parameters</span></span>

<span data-ttu-id="0767b-107">Keine</span><span class="sxs-lookup"><span data-stu-id="0767b-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0767b-108">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="0767b-108">Return value</span></span>

<span data-ttu-id="0767b-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="0767b-109">S_OK</span></span> 
  
> <span data-ttu-id="0767b-110">Das Formular wurde geändert, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="0767b-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="0767b-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="0767b-111">S_FALSE</span></span> 
  
> <span data-ttu-id="0767b-112">Das Formular hat keine Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="0767b-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0767b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0767b-113">Remarks</span></span>

<span data-ttu-id="0767b-114">Formular Viewer rufen Sie die **IPersistMessage::IsDirty** -Methode, um zu bestimmen, ob die Nachricht Daten vorliegen.</span><span class="sxs-lookup"><span data-stu-id="0767b-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0767b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0767b-115">See also</span></span>



[<span data-ttu-id="0767b-116">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0767b-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

