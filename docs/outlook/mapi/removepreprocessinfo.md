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
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432947"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="81ea8-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="81ea8-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="81ea8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81ea8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81ea8-105">Entfernt vorverarbeitete Informationen, die von einer [PreprocessMessage](preprocessmessage.md) -basierten Funktion geschrieben wurden, aus einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="81ea8-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81ea8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="81ea8-106">Header file:</span></span>  <br/> |<span data-ttu-id="81ea8-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="81ea8-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="81ea8-108">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="81ea8-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="81ea8-109">Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="81ea8-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="81ea8-110">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="81ea8-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="81ea8-111">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="81ea8-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="81ea8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="81ea8-112">Parameters</span></span>

 <span data-ttu-id="81ea8-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="81ea8-113">_lpMessage_</span></span>
  
> <span data-ttu-id="81ea8-114">in Zeiger auf die vorverarbeitete Nachricht, von der die Informationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81ea8-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="81ea8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81ea8-115">Return value</span></span>

<span data-ttu-id="81ea8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="81ea8-116">S_OK</span></span>
  
> <span data-ttu-id="81ea8-117">Vorverarbeitete Informationen wurden erfolgreich entfernt.</span><span class="sxs-lookup"><span data-stu-id="81ea8-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81ea8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81ea8-118">Remarks</span></span>

<span data-ttu-id="81ea8-119">Der MAPI-Spooler Ruft eine auf **RemovePreprocessInfo**basierende Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="81ea8-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="81ea8-120">Ein Transportanbieter registriert die **RemovePreprocessInfo** -basierte Funktion bei der Registrierung der parallelen **PreprocessMessage** -basierten Funktion bei einem Aufruf der [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="81ea8-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="81ea8-121">Ein für die Fax-Übertragung geeignetes Bildrendering ist ein Beispiel für vorverarbeitete Informationen, die von einer durch den [PreprocessMessage](preprocessmessage.md)-Funktionsprototyp definierten Funktion geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="81ea8-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="81ea8-122">Der MAPI-Spooler ruft in der Regel eine **RemovePreprocessInfo** -Funktion nach dem Senden einer Nachricht ab, die vorverarbeitete Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="81ea8-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

