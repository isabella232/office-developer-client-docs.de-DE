---
title: Freigeben des Transportanbieters
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328385"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="a742e-103">Freigeben des Transportanbieters</span><span class="sxs-lookup"><span data-stu-id="a742e-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="a742e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a742e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a742e-105">Wenn MAPI oder der MAPI-Spooler mit einem Transportanmeldeobjekt abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="a742e-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="a742e-106">MAPI oder der MAPI-Spooler ruft die [IXPLogon::TransportLogoff-Methode des Transportanbieters](ixplogon-transportlogoff.md) auf.</span><span class="sxs-lookup"><span data-stu-id="a742e-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="a742e-107">Der Transportanbieter macht das status-Objekt ungültig, indem die [IMAPISupport::MakeInvalid-Methode](imapisupport-makeinvalid.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="a742e-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="a742e-108">Ob der Transportanbieter Nachrichtenobjekte ungültig macht, die zum Zeitpunkt des **TransportLogoff-Aufrufs** gesendet oder empfangen werden, hängt von den Flags ab, die an **TransportLogoff übergeben wurden.**</span><span class="sxs-lookup"><span data-stu-id="a742e-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="a742e-109">Der Transportanbieter ruft die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) des Supportobjekts auf, um die Zeile des Transportanbieters aus der Statustabelle zu entfernen und alle eindeutigen Bezeichner (UIDs), die mit der [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) festgelegt wurden, aus internen Tabellen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a742e-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="a742e-110">Dadurch wird die Anzahl der bekannten Anmeldeobjekte, die für dieses Anbieterobjekt aktiv sind, dekrementiert.</span><span class="sxs-lookup"><span data-stu-id="a742e-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="a742e-111">Wenn die Anzahl null erreicht, ruft MAPI die [IXPProvider::Shutdown-Methode](ixpprovider-shutdown.md) und **Release für** das Anbieterobjekt auf.</span><span class="sxs-lookup"><span data-stu-id="a742e-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="a742e-112">Wenn dies das letzte bekannte Anbieterobjekt war, das diese DLL für diesen Prozess verwendet, ruft MAPI die **FreeLibrary-Funktion** zu einem späteren Zeitpunkt in der DLL auf.</span><span class="sxs-lookup"><span data-stu-id="a742e-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="a742e-113">Der Arbeitsspeicher für das MAPI-Unterstützungsobjekt wird freigegeben, und die **Release-Methode des Supportobjekts gibt** zurück.</span><span class="sxs-lookup"><span data-stu-id="a742e-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="a742e-114">Die **TransportLogoff-Methode** gibt S_OK.</span><span class="sxs-lookup"><span data-stu-id="a742e-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="a742e-115">MAPI oder der MAPI-Spooler ruft **Release für** das Anmeldeobjekt des Transportanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="a742e-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="a742e-116">Der Arbeitsspeicher für das Objekt wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="a742e-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="a742e-117">MAPI oder der MAPI-Spooler ruft **FreeLibrary** für die Anbieter-DLL auf.</span><span class="sxs-lookup"><span data-stu-id="a742e-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="a742e-118">Zur Robustheit sollten die Anmelde- und Anbieterobjekte  in der Lage sein, endgültige Releaseaufrufe für sich selbst zu verarbeiten, ohne zuerst ihre **TransportLogoff-** oder **Shutdown-Methoden** aufrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a742e-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="a742e-119">Wenn **Release** in solchen Fällen aufgerufen wird, sollten Transportanbieter die Anrufe so behandeln, als ob **TransportLogoff** oder **Shutdown** mit einem Nullargument gefolgt von Release aufgerufen **worden wären.**</span><span class="sxs-lookup"><span data-stu-id="a742e-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

