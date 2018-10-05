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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386222"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="524ca-103">Freigeben des Transportanbieters</span><span class="sxs-lookup"><span data-stu-id="524ca-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="524ca-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="524ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="524ca-105">Wenn MAPI oder die MAPI-Warteschlange beendet eine Anmeldung Transportobjekt verwenden ist:</span><span class="sxs-lookup"><span data-stu-id="524ca-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="524ca-106">MAPI- oder die MAPI-Warteschlange der Adressbuchhierarchie [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="524ca-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="524ca-107">Der Transportdienst wird das Statusobjekt durch Aufrufen der Methode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) ungültig.</span><span class="sxs-lookup"><span data-stu-id="524ca-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="524ca-108">Ob der Adressbuchhierarchie Nachrichtenobjekte ungültig, die hängt gesendet oder empfangen zum Zeitpunkt des Anrufs **TransportLogoff** der Kennzeichen, die an **TransportLogoff**übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="524ca-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="524ca-109">Der Transportdienst Ruft die des Unterstützungsobjekts [IUnknown](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) -Methode zum Entfernen der Adressbuchhierarchie Zeile aus der Statustabelle und aus internen Tabellen eine beliebige eindeutige Bezeichner (UIDs), die mit der [IMAPISupport festgelegt wurden: SetProviderUID](imapisupport-setprovideruid.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="524ca-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="524ca-110">Es verringert die Anzahl der bekannten Logon-Objekten, die auf dieses Anbieterobjekt aktiv.</span><span class="sxs-lookup"><span data-stu-id="524ca-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="524ca-111">Wenn die Anzahl 0 (null) erreicht, ruft MAPI die [IXPProvider::Shutdown](ixpprovider-shutdown.md) -Methode und die **Freigabe** für das Provider-Objekt.</span><span class="sxs-lookup"><span data-stu-id="524ca-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="524ca-112">Wenn dies das letzte bekannte Anbieterobjekt verwenden diese DLL für diesen Prozess war, ruft MAPI **FreeLibrary** -Funktion der DLL zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="524ca-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="524ca-113">Speicher für das MAPI-Support-Objekt wird freigegeben und **Release** -Methode das Support-Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="524ca-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="524ca-114">Die **TransportLogoff** -Methode gibt S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="524ca-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="524ca-115">MAPI- oder die MAPI-Warteschlange ruft **Release** auf der Adressbuchhierarchie Anmeldung-Objekt.</span><span class="sxs-lookup"><span data-stu-id="524ca-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="524ca-116">Der Speicher für das Objekt wird freigegeben.</span><span class="sxs-lookup"><span data-stu-id="524ca-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="524ca-117">MAPI- oder die MAPI-Warteschlange ruft **FreeLibrary** auf der Provider-DLL.</span><span class="sxs-lookup"><span data-stu-id="524ca-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="524ca-118">Für Stabilität sollte die Anmeldung und Anbieter-Objekte endgültige **Version** Anrufe auf sich selbst ohne zuvor ihre **TransportLogoff** oder **zum Herunterfahren von** Methoden behandeln können.</span><span class="sxs-lookup"><span data-stu-id="524ca-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="524ca-119">Wenn in solchen Fällen **Release** aufgerufen wird, sollte Transportanbieter die Anrufe behandelt, als ob **TransportLogoff** oder **Herunterfahren** mit einem NULL-Argument gefolgt von **Release**aufgerufen wurde, hatte.</span><span class="sxs-lookup"><span data-stu-id="524ca-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

