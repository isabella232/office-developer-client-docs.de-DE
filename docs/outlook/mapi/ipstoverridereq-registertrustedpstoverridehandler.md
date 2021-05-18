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
description: 'Letzte Änderung: 24. Februar 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279535"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="5d6a5-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="5d6a5-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="5d6a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d6a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d6a5-105">Initiiert die Entsperrprozedur für eine Datei mit persönlichen Ordnern (PST).</span><span class="sxs-lookup"><span data-stu-id="5d6a5-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="5d6a5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d6a5-106">Parameters</span></span>

 <span data-ttu-id="5d6a5-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="5d6a5-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="5d6a5-108">[in] Ein Zeiger auf den Pfad einer Dynamic Link Library (DLL) eines Drittanbieters.</span><span class="sxs-lookup"><span data-stu-id="5d6a5-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="5d6a5-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="5d6a5-109">_pvClientData_</span></span>
  
> <span data-ttu-id="5d6a5-110">[in] Ein Zeiger auf Clientdaten, der vom PST-Anbieter an nachfolgende Aufrufe der HrTrustedPSTOverrideHandlerCallback-Funktion der DLL übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d6a5-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="5d6a5-111">Diese Clientdaten können von der DLL verwendet werden, um zu überprüfen, ob das PST entsperrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d6a5-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5d6a5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d6a5-112">Return value</span></span>

<span data-ttu-id="5d6a5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5d6a5-113">S_OK</span></span>
  
> <span data-ttu-id="5d6a5-114">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5d6a5-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d6a5-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d6a5-115">Remarks</span></span>

<span data-ttu-id="5d6a5-116">Die vom wzDllPath-Parameter angegebene DLL muss mit einem digitalen Zertifikat signiert werden.</span><span class="sxs-lookup"><span data-stu-id="5d6a5-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="5d6a5-117">Die DLL muss auch eine Funktion mit der folgenden Signatur exportieren.</span><span class="sxs-lookup"><span data-stu-id="5d6a5-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="5d6a5-118">Diese Funktion wird mit einem Zeiger auf das IMsgStore-Objekt für das PST, einem Zeiger auf ein IUnknown-Objekt, das die IPSTOVERRIDE1-Schnittstelle implementiert, und einem Zeiger auf die ursprünglich über pvClientData bereitgestellten Daten aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5d6a5-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="5d6a5-119">Weitere Informationen finden Sie unter Implementieren eines PST-Außerkraftsetzungshandlers zum Umgehen der [PSTDisableGrow-Richtlinie in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="5d6a5-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5d6a5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d6a5-120">See also</span></span>



[<span data-ttu-id="5d6a5-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d6a5-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="5d6a5-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5d6a5-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

