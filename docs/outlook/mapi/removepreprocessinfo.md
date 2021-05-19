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
# <a name="removepreprocessinfo"></a><span data-ttu-id="ca803-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="ca803-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="ca803-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca803-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca803-105">Entfernt vorverarbeitete Informationen, die von einer [PreprocessMessage-basierten](preprocessmessage.md) Funktion geschrieben wurden, aus einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ca803-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca803-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ca803-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca803-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ca803-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ca803-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ca803-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="ca803-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="ca803-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="ca803-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="ca803-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="ca803-111">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="ca803-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="ca803-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca803-112">Parameters</span></span>

 <span data-ttu-id="ca803-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ca803-113">_lpMessage_</span></span>
  
> <span data-ttu-id="ca803-114">[in] Zeiger auf die vorverarbeitete Nachricht, aus der Informationen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ca803-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca803-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca803-115">Return value</span></span>

<span data-ttu-id="ca803-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca803-116">S_OK</span></span>
  
> <span data-ttu-id="ca803-117">Vorverarbeitete Informationen wurden erfolgreich entfernt.</span><span class="sxs-lookup"><span data-stu-id="ca803-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca803-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca803-118">Remarks</span></span>

<span data-ttu-id="ca803-119">Der MAPI-Spooler ruft eine Funktion basierend auf **RemovePreprocessInfo auf.**</span><span class="sxs-lookup"><span data-stu-id="ca803-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="ca803-120">Ein Transportanbieter registriert die **RemovePreprocessInfo-basierte** Funktion gleichzeitig, wenn er die parallele **PreprocessMessage-basierte** Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor-Methode](imapisupport-registerpreprocessor.md) registriert.</span><span class="sxs-lookup"><span data-stu-id="ca803-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="ca803-121">Ein Bildrendering, das für die Faxübertragung geeignet ist, ist ein Beispiel für vorverarbeitete Informationen, die von einer Funktion geschrieben wurden, die durch den Prototyp der [PreprocessMessage-Funktion](preprocessmessage.md)definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ca803-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="ca803-122">Der MAPI-Spooler ruft in der Regel eine **RemovePreprocessInfo-Funktion** auf, nachdem eine Nachricht mit vorverarbeiteten Informationen gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ca803-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

