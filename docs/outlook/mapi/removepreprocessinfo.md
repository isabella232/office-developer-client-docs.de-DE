---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588832"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="9514d-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="9514d-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="9514d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9514d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9514d-105">Entfernt vorverarbeitet Informationen von einer [PreprocessMessage](preprocessmessage.md) Basis-Funktion aus einer Nachricht verfasst.</span><span class="sxs-lookup"><span data-stu-id="9514d-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9514d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9514d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9514d-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="9514d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="9514d-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="9514d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="9514d-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="9514d-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="9514d-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="9514d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="9514d-111">MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="9514d-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="9514d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9514d-112">Parameters</span></span>

 <span data-ttu-id="9514d-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9514d-113">_lpMessage_</span></span>
  
> <span data-ttu-id="9514d-114">[in] Zeiger auf die vorverarbeiteten Nachricht aus der Informationen sind, entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9514d-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9514d-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="9514d-115">Return value</span></span>

<span data-ttu-id="9514d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="9514d-116">S_OK</span></span>
  
> <span data-ttu-id="9514d-117">Vorverarbeitete Informationen wurde erfolgreich entfernt.</span><span class="sxs-lookup"><span data-stu-id="9514d-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9514d-118">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="9514d-118">Remarks</span></span>

<span data-ttu-id="9514d-119">Die MAPI-Warteschlange Ruft eine Funktion basierend auf **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="9514d-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="9514d-120">Ein Transportdienstes registriert die Funktion **RemovePreprocessInfo** basierend gleichzeitig die parallele **PreprocessMessage** Basis-Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert.</span><span class="sxs-lookup"><span data-stu-id="9514d-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="9514d-121">Ein Bild rendern geeignet für die Übertragung von Fax ist ein Beispiel der vorverarbeiteten Informationen, die von einer Funktion, die von der [PreprocessMessage](preprocessmessage.md)Funktionsprototyp definierten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9514d-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="9514d-122">Die MAPI-Warteschlange Ruft eine **RemovePreprocessInfo** -Funktion in der Regel nach dem Senden einer Nachricht, die vorverarbeiteten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="9514d-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

