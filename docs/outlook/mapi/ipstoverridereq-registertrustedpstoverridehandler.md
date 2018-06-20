---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Zuletzt geändert: 24 Februar 2013'
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792809"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="8a20c-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="8a20c-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="8a20c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a20c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a20c-105">Initiiert das Aufheben der Sperre Verfahren für den persönlichen Ordner (PST).</span><span class="sxs-lookup"><span data-stu-id="8a20c-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="8a20c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a20c-106">Parameters</span></span>

 <span data-ttu-id="8a20c-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="8a20c-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="8a20c-108">[in] Ein Zeiger auf den Pfad zu einer Drittanbieter-Dynamic-Link Library (DLL).</span><span class="sxs-lookup"><span data-stu-id="8a20c-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="8a20c-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="8a20c-109">_pvClientData_</span></span>
  
> <span data-ttu-id="8a20c-110">[in] Ein Zeiger auf die Clientdaten, die vom Anbieter PST in nachfolgende Aufrufe an die DLL HrTrustedPSTOverrideHandlerCallback Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8a20c-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="8a20c-111">Diese Clientdaten können von der DLL verwendet werden, zur Unterstützung beim Überprüfen, ob die PST-Datei aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a20c-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a20c-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8a20c-112">Return value</span></span>

<span data-ttu-id="8a20c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a20c-113">S_OK</span></span>
  
> <span data-ttu-id="8a20c-114">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8a20c-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a20c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8a20c-115">Remarks</span></span>

<span data-ttu-id="8a20c-116">Der WzDllPath-Parameter angegebene DLL-Datei muss mit einem digitalen Zertifikat signiert werden.</span><span class="sxs-lookup"><span data-stu-id="8a20c-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="8a20c-117">Die DLL muss auch eine Funktion mit der folgenden Signatur exportieren.</span><span class="sxs-lookup"><span data-stu-id="8a20c-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="8a20c-118">Diese Funktion wird mit einen Zeiger auf das IMsgStore-Objekt für die PST-Datei, einen Zeiger auf eine IUnknown-Objekt, das die IPSTOVERRIDE1-Schnittstelle implementiert und einen Zeiger auf die Daten, die ursprünglich zur Verfügung gestellten PvClientData aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8a20c-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="8a20c-119">Weitere Informationen finden Sie unter [ein PST Außerkraftsetzung Handler für die Umgehung die PSTDisableGrow Richtlinie in Outlook 2007 implementiert wird](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="8a20c-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a20c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a20c-120">See also</span></span>



[<span data-ttu-id="8a20c-121">IPSTOVERRIDE1: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a20c-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="8a20c-122">IPSTOVERRIDEREQ: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a20c-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

