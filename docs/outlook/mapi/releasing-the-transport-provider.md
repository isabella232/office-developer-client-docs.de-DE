---
title: Freigeben des Transport Anbieters
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
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="83d17-103">Freigeben des Transport Anbieters</span><span class="sxs-lookup"><span data-stu-id="83d17-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="83d17-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83d17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83d17-105">Wenn MAPI oder der MAPI-Spooler mit einem Transport Logon-Objekt abgeschlossen ist:</span><span class="sxs-lookup"><span data-stu-id="83d17-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="83d17-106">MAPI oder der MAPI-Spooler Ruft die [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) -Methode des Transportanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="83d17-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="83d17-107">Der Transportanbieter validiert das Status-Objekt durch Aufrufen der [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="83d17-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="83d17-108">Ob der Transportanbieter Nachrichtenobjekte, die gesendet oder empfangen werden, zum Zeitpunkt des **TransportLogoff** -Aufrufs ungültig macht, hängt von den Flags ab, die an **TransportLogoff**übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="83d17-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="83d17-109">Der Transportanbieter Ruft die [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode des Support Objekts auf, um die Zeile des Transportanbieters aus der Statustabelle zu entfernen und aus internen Tabellen alle eindeutigen Bezeichner (IDs) zu entfernen, die mit der IMAPISupport festgelegt wurden [: SetProviderUID](imapisupport-setprovideruid.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="83d17-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="83d17-110">Die Anzahl bekannter Anmeldeobjekte, die für dieses Anbieterobjekt aktiv sind, wird verringert.</span><span class="sxs-lookup"><span data-stu-id="83d17-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="83d17-111">Wenn die Anzahl 0 (null) erreicht, ruft MAPI die [IXPProvider:: Shutdown](ixpprovider-shutdown.md) -Methode und die **Freigabe** für das Provider-Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="83d17-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="83d17-112">Wenn dies das letzte bekannte Anbieterobjekt ist, das diese DLL verwendet, ruft MAPI zu einem späteren Zeitpunkt die **FreeLibrary** -Funktion für die dll auf.</span><span class="sxs-lookup"><span data-stu-id="83d17-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="83d17-113">Der Speicher für das MAPI-Unterstützungsobjekt wird freigegeben, und die **Release** -Methode des Support-Objekts gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="83d17-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="83d17-114">Die **TransportLogoff** -Methode gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="83d17-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="83d17-115">MAPI oder der MAPI-Spooler Ruft die **Freigabe** für das Anmeldeobjekt des Transportanbieters auf.</span><span class="sxs-lookup"><span data-stu-id="83d17-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="83d17-116">Der Arbeitsspeicher für das Objekt wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="83d17-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="83d17-117">MAPI oder der MAPI-Spooler ruft **FreeLibrary** für die Anbieter-DLL auf.</span><span class="sxs-lookup"><span data-stu-id="83d17-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="83d17-118">Aus Stabilitäts-, Anmelde-und Anbieter Objekten sollte in der Lage sein, abschließende **Freigabe** Aufrufe für sich selbst zu behandeln, ohne zuvor Ihre **TransportLogoff** -oder **Shutdown** -Methoden aufgerufen zu haben.</span><span class="sxs-lookup"><span data-stu-id="83d17-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="83d17-119">Wenn **Release** in solchen Fällen aufgerufen wird, sollten Transportanbieter die Aufrufe so behandeln, als ob **TransportLogoff** oder **Shutdown** mit einem NULL-Argument, gefolgt von **Release**, aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="83d17-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

