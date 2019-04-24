---
title: Überprüfen der Dienstanbieterkonfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329607"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="9b9fd-103">Überprüfen der Dienstanbieterkonfiguration</span><span class="sxs-lookup"><span data-stu-id="9b9fd-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="9b9fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b9fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b9fd-105">Ihre Anmeldemethode ([IABProvider:: LOGON](iabprovider-logon.md), [IMSProvider:: LOGON](imsprovider-logon.md)oder [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md)) muss die Konfiguration Ihres Anbieters überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="9b9fd-106">Dabei wird überprüft, ob alle für den vollständigen Vorgang erforderlichen Eigenschaften richtig festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="9b9fd-107">Jeder Anbieter benötigt eine unterschiedliche Anzahl von Eigenschaften; die Konfiguration hängt von Ihrem Anbieter und dem Grad der zulässigen Benutzerinteraktion ab.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="9b9fd-108">Einige Dienstanbieter behalten alle erforderlichen Eigenschaften im Profil bei.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="9b9fd-109">Andere Dienstanbieter behalten eine partielle Gruppe von Eigenschaften im Profil bei und fordern den Benutzer auf, fehlende Werte einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="9b9fd-110">Dennoch werden von anderen Anbietern keine Eigenschaften im Profil gespeichert, und der Benutzer muss alle für die Konfiguration erforderlichen Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="9b9fd-111">So rufen Sie im Profil gespeicherte Eigenschaften ab</span><span class="sxs-lookup"><span data-stu-id="9b9fd-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="9b9fd-112">Rufen Sie [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)auf, und übergeben Sie die [MAPIUID](mapiuid.md) Ihres Anbieters als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="9b9fd-113">Rufen Sie die Methoden [IMAPIProp::](imapiprop-getprops.md) GetProps oder [IMAPIProp::](imapiprop-getproplist.md) getproplist des profile-Abschnitts auf, um einzelne Eigenschaften oder eine Eigenschaftenliste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="9b9fd-114">So legen Sie Eigenschaften aus Benutzerinformationen fest</span><span class="sxs-lookup"><span data-stu-id="9b9fd-114">To set properties from user information</span></span>
  
<span data-ttu-id="9b9fd-115">Zeigt ein Eigenschaftenfenster an, wenn MAPI kein Flag festgelegt hat, das die Anzeige verhindert.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="9b9fd-116">Die folgenden Flags zeigen an, dass eine Benutzeroberfläche nicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="9b9fd-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9b9fd-117">**Flag**</span></span>|<span data-ttu-id="9b9fd-118">**Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="9b9fd-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b9fd-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9b9fd-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="9b9fd-120">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="9b9fd-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="9b9fd-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9b9fd-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="9b9fd-122">Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="9b9fd-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="9b9fd-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9b9fd-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="9b9fd-124">Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="9b9fd-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="9b9fd-125">Wenn Ihr Anbieter nicht alle Konfigurationseigenschaften im Profil speichert, eine Benutzerinteraktion erfordert und MAPI eines der Dialogfeld Unterdrückungs Kennzeichen an Ihre Anmeldemethode übergibt, geben Sie MAPI_E_UNCONFIGURED zurück.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="9b9fd-126">Geben Sie auch diesen Fehler zurück, wenn das Dialogfeld Unterdrückungs Kennzeichen nicht festgelegt ist, aber der Benutzer nicht alle erforderlichen Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="9b9fd-127">Wenn der Dienstanbieter seine Anmeldemethode mit MAPI_E_UNCONFIGURED nicht unterbricht, ruft MAPI ihre Einstiegspunktfunktion erneut auf.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="9b9fd-128">Wenn die Informationen beim zweiten Aufruf nicht gefunden werden können, wird die Sitzung möglicherweise beendet, je nachdem, wie wichtig der Dienstanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="9b9fd-129">Die folgende Abbildung zeigt die Logik, die für die Konfiguration in ihrer Dienstanbieter-Anmeldemethode erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9b9fd-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="9b9fd-130">**Flussdiagramm für Konfigurationsüberprüfung**</span><span class="sxs-lookup"><span data-stu-id="9b9fd-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="9b9fd-131">![Flussdiagramm zur Konfigurationsüberprüfung] (media/amapi_62.gif "Flussdiagramm zur Konfigurationsüberprüfung")</span><span class="sxs-lookup"><span data-stu-id="9b9fd-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b9fd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b9fd-132">See also</span></span>

- [<span data-ttu-id="9b9fd-133">Implementieren der Dienstanbieter Anmeldung</span><span class="sxs-lookup"><span data-stu-id="9b9fd-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

