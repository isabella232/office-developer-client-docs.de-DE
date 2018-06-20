---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0ddff638e26940ea74932a8a491455f67cc8dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793112"
---
# <a name="mapierror"></a><span data-ttu-id="d9b4f-103">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d9b4f-103">MAPIERROR</span></span>

  
  
<span data-ttu-id="d9b4f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9b4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9b4f-105">Enthält ausführliche Informationen zu einem Fehler, die in der Regel durch das Betriebssystem, MAPI- oder einem Dienstanbieter generiert.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-105">Provides detailed information about an error, typically generated by the operating system, MAPI, or a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9b4f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d9b4f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9b4f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9b4f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a><span data-ttu-id="d9b4f-108">Members</span><span class="sxs-lookup"><span data-stu-id="d9b4f-108">Members</span></span>

 <span data-ttu-id="d9b4f-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-109">**ulVersion**</span></span>
  
> <span data-ttu-id="d9b4f-110">Versionsnummer der Struktur.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-110">Version number of the structure.</span></span> <span data-ttu-id="d9b4f-111">Der **UlVersion** Member wird für die zukünftige Erweiterung verwendet und sollte auf MAPI_ERROR_VERSION, derzeit definiert als 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-111">The **ulVersion** member is used for future expansion and should be set to MAPI_ERROR_VERSION, which is currently defined as zero.</span></span> 
    
 <span data-ttu-id="d9b4f-112">**lpszError**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-112">**lpszError**</span></span>
  
> <span data-ttu-id="d9b4f-113">Zeiger auf eine Zeichenfolge, die den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-113">Pointer to a string that describes the error.</span></span> <span data-ttu-id="d9b4f-114">Diese Zeichenfolge wird im Unicode-Format sein, wenn der Parameter _UlFlags_ an die-Methode, in der diese Struktur verwendet wird, auf Parameter MAPI_UNICODE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-114">This string will be in Unicode format if the  _ulFlags_ parameter to the method in which this structure is used is set to MAPI_UNICODE.</span></span> 
    
 <span data-ttu-id="d9b4f-115">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-115">**lpszComponent**</span></span>
  
> <span data-ttu-id="d9b4f-116">Zeiger auf eine Zeichenfolge, die die Komponente beschreibt, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-116">Pointer to a string that describes the component that generated the error.</span></span> <span data-ttu-id="d9b4f-117">Diese Zeichenfolge wird im Unicode-Format sein, wenn der Parameter _UlFlags_ an die-Methode, in der diese Struktur verwendet wird, auf Parameter MAPI_UNICODE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-117">This string will be in Unicode format if the  _ulFlags_ parameter to the method in which this structure is used is set to MAPI_UNICODE.</span></span> 
    
 <span data-ttu-id="d9b4f-118">**ulLowLevelError**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-118">**ulLowLevelError**</span></span>
  
> <span data-ttu-id="d9b4f-119">Low-Level Fehlerwert, der verwendet wird, nur, wenn der Fehler zurückgegeben werden soll auf niedriger Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-119">Low-level error value that is used only when the error to be returned is low-level.</span></span>
    
 <span data-ttu-id="d9b4f-120">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="d9b4f-120">**ulContext**</span></span>
  
> <span data-ttu-id="d9b4f-121">Wert, der die Position in der Komponente darstellt, auf die der **LpszComponent** -Member, der angibt, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-121">Value that represents the location in the component pointed to by the **lpszComponent** member that identifies where the error occurred.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d9b4f-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9b4f-122">Remarks</span></span>

<span data-ttu-id="d9b4f-123">Die Struktur **MAPIERROR** wird verwendet, um die Fehlerinformationen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-123">The **MAPIERROR** structure is used to describe error information.</span></span> <span data-ttu-id="d9b4f-124">Clients und Dienstanbieter übergeben einen Zeiger auf eine **MAPIERROR** -Struktur in der _LppMAPIError_ -Parameter der [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-124">Clients and service providers pass a pointer to a **MAPIERROR** structure in the  _lppMAPIError_ parameter of the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> <span data-ttu-id="d9b4f-125">**GetLastError** gibt Informationen zu den vorherigen auf ein Objekt aufgetretenen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-125">**GetLastError** returns information about the previous error that has occurred to an object.</span></span> <span data-ttu-id="d9b4f-126">**GetLastError** Aufrufer freigeben den Speicher für die Struktur **MAPIERROR** durch Aufrufen von [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="d9b4f-126">Callers of **GetLastError** free the memory for the **MAPIERROR** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
<span data-ttu-id="d9b4f-127">Der **LpszComponent** Member kann die Komponente Hilfedatei zuordnen verwendet werden, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-127">The **lpszComponent** member can be used to map the component's Help file, if one exists.</span></span> <span data-ttu-id="d9b4f-128">Dienstanbieter sollte die Größe der Komponente Zeichenfolge auf 30 Zeichen einschränken, sodass es auf einfache Weise in einem Dialogfeld angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-128">Service providers should limit the size of the component string to 30 characters so that it can easily be displayed in a dialog box.</span></span> <span data-ttu-id="d9b4f-129">Das **UlContext** -Element kann auch verweisen auf ein Thema der Onlinehilfe für häufige Fehler verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-129">The **ulContext** member can also be used to refer to an online Help topic for common errors.</span></span> 
  
<span data-ttu-id="d9b4f-130">Dienstanbieter sind nicht erforderlich, um ausführliche Fehlerinformationen bereitzustellen, sollten Clients keine Member der Struktur **MAPIERROR** erwarten, die zurückgegeben werden, um gültige Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-130">Because service providers are not required to provide detailed error information, clients should not expect any of the members of the **MAPIERROR** structure that are returned to contain valid data.</span></span> <span data-ttu-id="d9b4f-131">Allerdings empfiehlt unter minimale MAPI, Anbieter Informationen im **LpszComponent** und **UlContext** -Member angeben.</span><span class="sxs-lookup"><span data-stu-id="d9b4f-131">However, at a minimum MAPI strongly recommends that providers specify information in the **lpszComponent** and **ulContext** members.</span></span> 
  
<span data-ttu-id="d9b4f-132">Weitere Informationen zur Fehlerbehandlung in MAPI finden Sie unter [Fehlerbehandlung](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="d9b4f-132">For more information about error handling in MAPI, see [Error Handling](error-handling-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9b4f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9b4f-133">See also</span></span>



[<span data-ttu-id="d9b4f-134">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-134">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="d9b4f-135">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d9b4f-135">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="d9b4f-136">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-136">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="d9b4f-137">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-137">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="d9b4f-138">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-138">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="d9b4f-139">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-139">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="d9b4f-140">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="d9b4f-140">IMAPISupport::OpenAddressBook</span></span>](imapisupport-openaddressbook.md)
  
[<span data-ttu-id="d9b4f-141">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="d9b4f-141">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="d9b4f-142">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-142">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="d9b4f-143">IMsgServiceAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-143">IMsgServiceAdmin::GetLastError</span></span>](imsgserviceadmin-getlasterror.md)
  
[<span data-ttu-id="d9b4f-144">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-144">IMSLogon::GetLastError</span></span>](imslogon-getlasterror.md)
  
[<span data-ttu-id="d9b4f-145">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d9b4f-145">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="d9b4f-146">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-146">IProfAdmin::GetLastError</span></span>](iprofadmin-getlasterror.md)
  
[<span data-ttu-id="d9b4f-147">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d9b4f-147">IProviderAdmin::GetLastError</span></span>](iprovideradmin-getlasterror.md)


[<span data-ttu-id="d9b4f-148">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d9b4f-148">MAPI Structures</span></span>](mapi-structures.md)
