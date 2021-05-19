---
title: Überprüfen der Dienstanbieterkonfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418848"
---
# <a name="verifying-service-provider-configuration"></a><span data-ttu-id="3f902-103">Überprüfen der Dienstanbieterkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3f902-103">Verifying service provider configuration</span></span>
  
<span data-ttu-id="3f902-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f902-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f902-105">Ihre Anmeldemethode ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) muss die Konfiguration Ihres Anbieters überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3f902-105">Your logon method ([IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md), or [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) must verify your provider's configuration.</span></span> <span data-ttu-id="3f902-106">Dazu muss überprüft werden, ob alle eigenschaften, die für den vollständigen Betrieb erforderlich sind, ordnungsgemäß festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3f902-106">This involves checking that all of the properties needed for full operation are set correctly.</span></span> <span data-ttu-id="3f902-107">Jeder Anbieter benötigt eine andere Anzahl von Eigenschaften. die Konfiguration hängt von Ihrem Anbieter und dem Grad der Benutzerinteraktion ab, die Sie zulassen.</span><span class="sxs-lookup"><span data-stu-id="3f902-107">Every provider requires a different number of properties; configuration depends on your provider and the degree of user interaction you allow.</span></span> <span data-ttu-id="3f902-108">Einige Dienstanbieter behalten alle erforderlichen Eigenschaften im Profil bei.</span><span class="sxs-lookup"><span data-stu-id="3f902-108">Some service providers keep all of the necessary properties in the profile.</span></span> 

<span data-ttu-id="3f902-109">Andere Dienstanbieter behalten einen Teilsatz von Eigenschaften im Profil bei und fordert den Benutzer auf, fehlende Werte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3f902-109">Other service providers keep a partial set of properties in the profile and prompt the user for missing values.</span></span> <span data-ttu-id="3f902-110">Andere Anbieter speichern jedoch keine Eigenschaften im Profil und verlassen sich darauf, dass der Benutzer alle für die Konfiguration erforderlichen Informationen zur Verfügung hat.</span><span class="sxs-lookup"><span data-stu-id="3f902-110">Still other providers do not store properties in the profile at all, relying on the user to supply all of the information needed for configuration.</span></span>
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a><span data-ttu-id="3f902-111">So rufen Sie im Profil gespeicherte Eigenschaften ab</span><span class="sxs-lookup"><span data-stu-id="3f902-111">To retrieve properties stored in the profile</span></span>
  
1. <span data-ttu-id="3f902-112">Rufen [Sie IMAPISupport::OpenProfileSection auf,](imapisupport-openprofilesection.md)und übergeben Sie die [MAPIUID](mapiuid.md) Ihres Anbieters als Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="3f902-112">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), passing the [MAPIUID](mapiuid.md) of your provider as an input parameter.</span></span> 
    
2. <span data-ttu-id="3f902-113">Rufen Sie die [IMAPIProp::GetProps-](imapiprop-getprops.md) oder [IMAPIProp::GetPropList-Methoden](imapiprop-getproplist.md) des Profilabschnitts auf, um einzelne Eigenschaften oder eine Eigenschaftenliste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3f902-113">Call the profile section's [IMAPIProp::GetProps](imapiprop-getprops.md) or [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods to retrieve individual properties or a property list.</span></span> 
    
### <a name="to-set-properties-from-user-information"></a><span data-ttu-id="3f902-114">So legen Sie Eigenschaften aus Benutzerinformationen</span><span class="sxs-lookup"><span data-stu-id="3f902-114">To set properties from user information</span></span>
  
<span data-ttu-id="3f902-115">Zeigen Sie ein Eigenschaftenblatt an, wenn MAPI kein Flag festgelegt hat, das die Anzeige verbietet.</span><span class="sxs-lookup"><span data-stu-id="3f902-115">Display a property sheet, if MAPI has not set a flag prohibiting the display.</span></span> <span data-ttu-id="3f902-116">Die folgenden Flags deuten darauf hin, dass keine Benutzeroberfläche angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f902-116">The following flags indicate that a user interface cannot be presented.</span></span>
  
|<span data-ttu-id="3f902-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3f902-117">**Flag**</span></span>|<span data-ttu-id="3f902-118">**Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="3f902-118">**Service provider**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f902-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="3f902-119">AB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="3f902-120">Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="3f902-120">Address book provider</span></span>  <br/> |
|<span data-ttu-id="3f902-121">LOGON_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="3f902-121">LOGON_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="3f902-122">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="3f902-122">Transport provider</span></span>  <br/> |
|<span data-ttu-id="3f902-123">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="3f902-123">MDB_NO_DIALOG</span></span>  <br/> |<span data-ttu-id="3f902-124">Anbieter des Nachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="3f902-124">Message store provider</span></span>  <br/> |
   
<span data-ttu-id="3f902-125">Wenn Ihr Anbieter nicht alle Konfigurationseigenschaften im Profil gespeichert hat und eine Benutzerinteraktion erforderlich ist, und MAPI eines der Dialogfeldunterdrückungsflags an Ihre Anmeldemethode übergibt, geben Sie MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="3f902-125">If your provider does not store all of its configuration properties in the profile, requiring user interaction, and MAPI passes one of the dialog box suppression flags to your logon method, return MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="3f902-126">Geben Sie diesen Fehler auch zurück, wenn das Dialogfeldunterdrückungsflag nicht festgelegt ist, der Benutzer jedoch nicht alle erforderlichen Informationen zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="3f902-126">Also return this error when the dialog suppression flag is not set, but the user does not supply all of the required information.</span></span>
  
<span data-ttu-id="3f902-127">Wenn ihr Dienstanbieter seine Anmeldemethode mit MAPI_E_UNCONFIGURED, ruft MAPI ihre Einstiegspunktfunktion erneut auf.</span><span class="sxs-lookup"><span data-stu-id="3f902-127">When your service provider fails its logon method with MAPI_E_UNCONFIGURED, MAPI calls your entry point function again.</span></span> <span data-ttu-id="3f902-128">Wenn die Informationen beim zweiten Anruf nicht gespeichert werden können, wird die Sitzung möglicherweise beendet, je nachdem, wie wichtig Ihr Dienstanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="3f902-128">If the information cannot be located with the second call, the session might terminate, depending on how important your service provider is.</span></span> 
  
<span data-ttu-id="3f902-129">Die folgende Abbildung zeigt die logik, die für die Konfiguration in der Anmeldemethode des Dienstanbieters erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3f902-129">The following illustration shows the logic required for configuration in your service provider logon method.</span></span> 
  
<span data-ttu-id="3f902-130">**Flussdiagramm für Konfigurationsüberprüfung**</span><span class="sxs-lookup"><span data-stu-id="3f902-130">**Configuration verification flowchart**</span></span>
  
<span data-ttu-id="3f902-131">![Flussdiagramm zur Konfigurationsprüfung](media/amapi_62.gif "Konfigurationsüberprüfungsflussdiagramm")</span><span class="sxs-lookup"><span data-stu-id="3f902-131">![Configuration verification flowchart](media/amapi_62.gif "Configuration verification flowchart")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f902-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f902-132">See also</span></span>

- [<span data-ttu-id="3f902-133">Implementieren der Dienstanbieteranmeldung</span><span class="sxs-lookup"><span data-stu-id="3f902-133">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

