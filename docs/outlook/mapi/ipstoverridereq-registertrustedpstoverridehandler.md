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
description: 'Zuletzt geändert: 24 Februar, 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279535"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="5eca1-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="5eca1-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="5eca1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eca1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eca1-105">Initiiert das Entriegelungs Verfahren für eine persönliche Ordner-Datei (PST).</span><span class="sxs-lookup"><span data-stu-id="5eca1-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="5eca1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5eca1-106">Parameters</span></span>

 <span data-ttu-id="5eca1-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="5eca1-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="5eca1-108">in Ein Zeiger auf den Pfad einer DLL (Dynamic Link Library) eines Drittanbieters.</span><span class="sxs-lookup"><span data-stu-id="5eca1-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="5eca1-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="5eca1-109">_pvClientData_</span></span>
  
> <span data-ttu-id="5eca1-110">in Ein Zeiger auf Client Daten, der vom PST-Anbieter an nachfolgende Aufrufe der DLL-HrTrustedPSTOverrideHandlerCallback-Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5eca1-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="5eca1-111">Diese Client Daten können von der DLL verwendet werden, um zu überprüfen, ob die PST-Datei entsperrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eca1-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5eca1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5eca1-112">Return value</span></span>

<span data-ttu-id="5eca1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="5eca1-113">S_OK</span></span>
  
> <span data-ttu-id="5eca1-114">Der Funktionsaufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5eca1-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5eca1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5eca1-115">Remarks</span></span>

<span data-ttu-id="5eca1-116">Die vom wzDllPath-Parameter angegebene DLL muss mit einem digitalen Zertifikat signiert werden.</span><span class="sxs-lookup"><span data-stu-id="5eca1-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="5eca1-117">Die DLL muss eine Funktion auch mit der folgenden Signatur exportieren.</span><span class="sxs-lookup"><span data-stu-id="5eca1-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="5eca1-118">Diese Funktion wird mit einem Zeiger auf das IMsgStore-Objekt für die PST-Datei, einem Zeiger auf ein IUnknown-Objekt, das die IPSTOVERRIDE1-Schnittstelle implementiert, und einem Zeiger auf die Daten aufgerufen, die ursprünglich über pvClientData bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5eca1-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="5eca1-119">Weitere Informationen finden Sie unter [Implementieren eines PST-Überschreibungs Handlers, um die PSTDisableGrow-Richtlinie in Outlook 2007 zu umgehen](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="5eca1-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5eca1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eca1-120">See also</span></span>



[<span data-ttu-id="5eca1-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5eca1-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="5eca1-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5eca1-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

