---
title: Überprüfen der Konfiguration für Service provider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 047a3b99b2d615984252071a1264521a4b2240f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795838"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="927dc-103">Überprüfen der Konfiguration für Service provider</span><span class="sxs-lookup"><span data-stu-id="927dc-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="927dc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="927dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="927dc-105">Die Logon-Methode ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) muss vom Dienstanbieter Konfiguration überprüfen.</span><span class="sxs-lookup"><span data-stu-id="927dc-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="927dc-106">Dieser Schritt umfasst, überprüfen, dass alle Eigenschaften für die vollständige Vorgänge benötigt richtig eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="927dc-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="927dc-107">Jeder Anbieter erfordert eine unterschiedliche Anzahl von Eigenschaften. Konfiguration abhängig von Ihren Anbieter und den Grad der Benutzerinteraktion, für die Sie zulassen.</span><span class="sxs-lookup"><span data-stu-id="927dc-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="927dc-108">Einige Dienstanbieter lassen Sie alle erforderlichen Eigenschaften im Benutzerprofil.</span><span class="sxs-lookup"><span data-stu-id="927dc-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="927dc-109">Dienstanbieter lassen Sie eine Teilmenge der Eigenschaften im Benutzerprofil und auffordern, nach fehlenden Werten.</span><span class="sxs-lookup"><span data-stu-id="927dc-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="927dc-110">Noch speichern andere Anbieter Eigenschaften im Benutzerprofil in allen nicht auf dem Benutzer alle Informationen für die Konfiguration erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="927dc-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="927dc-111">Zum Abrufen von Eigenschaften, die im Profil gespeichert</span><span class="sxs-lookup"><span data-stu-id="927dc-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="927dc-112">Rufen Sie [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), die [MAPIUID](mapiuid.md) Ihres Anbieters als Eingabeparameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="927dc-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="927dc-113">Rufen Sie Profilabschnitt [IMAPIProp::GetProps](imapiprop-getprops.md) oder [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methoden zum Abrufen von einzelnen Eigenschaften oder eine Eigenschaftenliste auf.</span><span class="sxs-lookup"><span data-stu-id="927dc-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="927dc-114">Festlegen von Eigenschaften von Benutzerinformationen</span><span class="sxs-lookup"><span data-stu-id="927dc-114">To set properties from user information</span></span>
  
<span data-ttu-id="927dc-115">Ein Eigenschaftenblatt angezeigt, wenn MAPI ein Flag verbietet die Anzeige nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="927dc-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="927dc-116">Die folgenden Kennzeichen darauf hinzuweisen, dass eine Benutzeroberfläche nicht gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="927dc-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="927dc-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="927dc-117">**Flag**</span></span>|<span data-ttu-id="927dc-118">**Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="927dc-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="927dc-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="927dc-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="927dc-120">-Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="927dc-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="927dc-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="927dc-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="927dc-122">Transportdienst</span><span class="sxs-lookup"><span data-stu-id="927dc-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="927dc-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="927dc-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="927dc-124">Nachricht Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="927dc-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="927dc-125">Wenn vom Dienstanbieter speichert nicht alle seine Konfigurationseigenschaften in das Profil Benutzereingriff und MAPI zu den Dialogfeld Feld Unterdrückung Flags an Ihre Logon (Methode) übergibt, geben Sie MAPI_E_UNCONFIGURED zurück.</span><span class="sxs-lookup"><span data-stu-id="927dc-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="927dc-126">Zurückgegeben Sie dieser Fehler wird auch, wenn das Dialogfeld Unterdrückung Flag nicht festgelegt ist, aber der Benutzer nicht alle erforderlichen Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="927dc-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="927dc-127">Wenn die Logon-Methode mit MAPI_E_UNCONFIGURED Ihren Dienstanbieter ein Fehler auftritt, ruft MAPI erneut Ihre Entry Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="927dc-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="927dc-128">Wenn die Informationen nicht mit dem zweiten Aufruf gefunden werden kann, kann die Sitzung beenden, je nachdem, wie wichtig Ihren Dienstanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="927dc-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="927dc-129">Die folgende Abbildung zeigt die Logik für die Konfiguration in Ihrer Service Provider Logon (Methode) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="927dc-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="927dc-130">**Flussdiagramm für Konfigurationsüberprüfung**</span><span class="sxs-lookup"><span data-stu-id="927dc-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="927dc-131">![Flussdiagramm für konfigurationsüberprüfung] (media/amapi_62.gif "Flussdiagramm für konfigurationsüberprüfung")</span><span class="sxs-lookup"><span data-stu-id="927dc-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="927dc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="927dc-132">See also</span></span>

- [<span data-ttu-id="927dc-133">Implementieren einer Dienstanbieteranmeldung</span><span class="sxs-lookup"><span data-stu-id="927dc-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

