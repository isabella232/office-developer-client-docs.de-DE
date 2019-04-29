---
title: Transport Anbieter und MAPI-Spooler-Betriebsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426625"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="d53e6-103">Transport Anbieter und MAPI-Spooler-Betriebsmodell</span><span class="sxs-lookup"><span data-stu-id="d53e6-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="d53e6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d53e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d53e6-105">Transportanbieter Initialisierung, Start, Verarbeitung, Herunterfahren und Deinitialisierung werden durch eine Reihe von Aufrufen vom MAPI-Spooler an den Transportanbieter durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d53e6-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="d53e6-106">Die Anrufe werden wie folgt sequenziert:</span><span class="sxs-lookup"><span data-stu-id="d53e6-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="d53e6-107">Der MAPI-Spooler Ruft die [XPProviderInit](xpproviderinit.md) -Funktion auf, übergibt ein Support-Objekt, ruft das Anbieterobjekt ab und überprüft, ob der Transportanbieter und der MAPI-Spooler einen kompatiblen MAPI-Versions Nummerntyp unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d53e6-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="d53e6-108">Der MAPI-Spooler Ruft die [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) -Methode der [IXPProvider: IUnknown](ixpprovideriunknown.md) -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="d53e6-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="d53e6-109">Zwischen dem MAPI-Spooler und dem Transportanbieter wird eine Sitzung mit den Anmeldeinformationen im aktuellen Abschnitt des Profils eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="d53e6-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="d53e6-110">Der Transportanbieter gibt ein LOGON-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d53e6-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="d53e6-111">Die MAPI-Warteschlange ruft die [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d53e6-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="d53e6-112">Der Transportanbieter gibt eine Liste der eindeutigen Bezeichner (IDs) und e-Mail-Adresstypen zurück, die er akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d53e6-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="d53e6-113">Der Transportanbieter Ruft die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode auf, um die Zeile in der MAPI-Statustabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d53e6-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="d53e6-114">Die MAPI-Warteschlange ruft die [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode auf, um die Nachrichtenübertragung und den Empfang zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d53e6-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="d53e6-115">Wenn der Transportanbieter in seiner Rückgabe für den **TransportLogon** -Aufruf angefordert wird, ruft der MAPI-Spooler in regelmäßigen Abständen die [IXPLogon:: idle](ixplogon-idle.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="d53e6-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="d53e6-116">Die Leerlaufverarbeitung ist nützlich, wenn der Transportanbieter das zugrunde liegende Messagingsystem auf neue Nachrichten Abfragen oder andere Aufgaben mit niedriger Priorität ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="d53e6-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="d53e6-117">Die MAPI-Warteschlange und der Transportanbieter senden und empfangen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d53e6-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="d53e6-118">Weitere Informationen finden Sie unter [Nachrichten Übermittlungs Modell](message-submission-model.md) und [Nachrichtenempfangs Modell](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="d53e6-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="d53e6-119">Die MAPI-Warteschlangendienste transportieren Anforderungen und Aufrufe für Support-, Message-und Attachment-Objekte.</span><span class="sxs-lookup"><span data-stu-id="d53e6-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="d53e6-120">Die MAPI-Warteschlange ruft die **TransportNotify** -Methode auf, um die Nachrichtenübertragung und den Empfang zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d53e6-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="d53e6-121">Der MAPI-Spooler gibt die Objekte LOGON und Provider frei.</span><span class="sxs-lookup"><span data-stu-id="d53e6-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="d53e6-122">Weitere Informationen finden Sie unter der [IXPProvider:: Shutdown](ixpprovider-shutdown.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d53e6-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

