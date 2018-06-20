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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795395"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="81f93-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="81f93-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="81f93-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81f93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81f93-105">Entfernt vorverarbeitet Informationen von einer [PreprocessMessage](preprocessmessage.md) Basis-Funktion aus einer Nachricht verfasst.</span><span class="sxs-lookup"><span data-stu-id="81f93-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81f93-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="81f93-106">Header file:</span></span>  <br/> |<span data-ttu-id="81f93-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="81f93-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="81f93-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="81f93-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="81f93-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="81f93-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="81f93-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="81f93-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="81f93-111">MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="81f93-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="81f93-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="81f93-112">Parameters</span></span>

 <span data-ttu-id="81f93-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="81f93-113">_lpMessage_</span></span>
  
> <span data-ttu-id="81f93-114">[in] Zeiger auf die vorverarbeiteten Nachricht aus der Informationen sind, entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="81f93-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81f93-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="81f93-115">Return value</span></span>

<span data-ttu-id="81f93-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="81f93-116">S_OK</span></span>
  
> <span data-ttu-id="81f93-117">Vorverarbeitete Informationen wurde erfolgreich entfernt.</span><span class="sxs-lookup"><span data-stu-id="81f93-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81f93-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81f93-118">Remarks</span></span>

<span data-ttu-id="81f93-119">Die MAPI-Warteschlange Ruft eine Funktion basierend auf **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="81f93-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="81f93-120">Ein Transportdienstes registriert die Funktion **RemovePreprocessInfo** basierend gleichzeitig die parallele **PreprocessMessage** Basis-Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert.</span><span class="sxs-lookup"><span data-stu-id="81f93-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="81f93-121">Ein Bild rendern geeignet für die Übertragung von Fax ist ein Beispiel der vorverarbeiteten Informationen, die von einer Funktion, die von der [PreprocessMessage](preprocessmessage.md)Funktionsprototyp definierten geschrieben.</span><span class="sxs-lookup"><span data-stu-id="81f93-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="81f93-122">Die MAPI-Warteschlange Ruft eine **RemovePreprocessInfo** -Funktion in der Regel nach dem Senden einer Nachricht, die vorverarbeiteten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="81f93-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

