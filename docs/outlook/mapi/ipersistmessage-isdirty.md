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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407571"
---
# <a name="ipersistmessageisdirty"></a><span data-ttu-id="10dde-103">IPersistMessage::IsDirty</span><span class="sxs-lookup"><span data-stu-id="10dde-103">IPersistMessage::IsDirty</span></span>

  
  
<span data-ttu-id="10dde-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10dde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10dde-105">Überprüft das Formular auf Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="10dde-105">Checks the form for changes that were made since the last save.</span></span>
  
```cpp
HRESULT IsDirty( void );
```

## <a name="parameters"></a><span data-ttu-id="10dde-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10dde-106">Parameters</span></span>

<span data-ttu-id="10dde-107">Keine</span><span class="sxs-lookup"><span data-stu-id="10dde-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="10dde-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10dde-108">Return value</span></span>

<span data-ttu-id="10dde-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="10dde-109">S_OK</span></span> 
  
> <span data-ttu-id="10dde-110">Das Formular hat Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="10dde-110">The form has changes that were made since it was last saved.</span></span>
    
<span data-ttu-id="10dde-111">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="10dde-111">S_FALSE</span></span> 
  
> <span data-ttu-id="10dde-112">Das Formular enthält keine Änderungen, die seit dem letzten Speichern vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="10dde-112">The form does not have changes that were made since it was last saved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10dde-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10dde-113">Remarks</span></span>

<span data-ttu-id="10dde-114">Formularbetrachter rufen die **IPersistMessage::IsDirty-Methode** auf, um zu bestimmen, ob die Nachricht nicht gespeicherte Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="10dde-114">Form viewers call the **IPersistMessage::IsDirty** method to determine whether the message has unsaved data.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="10dde-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10dde-115">See also</span></span>



[<span data-ttu-id="10dde-116">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="10dde-116">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

