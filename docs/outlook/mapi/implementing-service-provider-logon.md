---
title: Implementieren der Dienstanbieteranmeldung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310087"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="bc9f3-103">Implementieren der Dienstanbieteranmeldung</span><span class="sxs-lookup"><span data-stu-id="bc9f3-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="bc9f3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc9f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc9f3-105">MAPI ruft eine Methode in Ihrem Anbieterobjekt auf, um den Anmeldevorgang mithilfe des Zeigers zu beginnen, den Sie von Ihrer Einstiegspunktfunktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="bc9f3-106">Die Methode variiert je nach Typ Ihres Dienstanbieters wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bc9f3-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="bc9f3-107">[IABProvider::Anmeldung](iabprovider-logon.md) für Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="bc9f3-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="bc9f3-108">[IMSProvider::Anmeldung für](imsprovider-logon.md) Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="bc9f3-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="bc9f3-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) für Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="bc9f3-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="bc9f3-110">Führen Sie die folgenden Aufgaben in der von Ihnen implementierten Anmeldemethode aus:</span><span class="sxs-lookup"><span data-stu-id="bc9f3-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="bc9f3-111">Erhöhen Sie die Referenzanzahl für das Supportobjekt, das als Eingabeparameter übergeben wird, indem Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="bc9f3-112">Rufen Sie die [IMAPISupport::OpenProfileSection-Methode des Supportobjekts](imapisupport-openprofilesection.md) auf, um auf Ihren Profilabschnitt zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="bc9f3-113">Rufen Sie die [IMAPIProp::SetProps-Methode des Profilabschnitts auf,](imapiprop-setprops.md) um die folgenden Eigenschaften zu setzen:</span><span class="sxs-lookup"><span data-stu-id="bc9f3-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="bc9f3-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc9f3-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="bc9f3-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc9f3-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="bc9f3-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc9f3-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="bc9f3-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="bc9f3-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="bc9f3-118">Versuchen Sie nicht, die Eigenschaften des **Profilabschnitts PR_RESOURCE_FLAGS** **PR_PROVIDER_DLL_NAME** festlegen.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="bc9f3-119">Bei der Anmeldung sind diese Eigenschaften schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="bc9f3-120">Überprüfen Sie, ob die eigenschaften, die Sie für die Konfiguration benötigen, entweder im Profil gespeichert sind oder vom Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="bc9f3-121">Weitere Informationen zum Überprüfen der Konfiguration finden Sie unter [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="bc9f3-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="bc9f3-122">Rufen Sie die [IMAPISupport::SetProviderUID-Methode](imapisupport-setprovideruid.md) des Supportobjekts auf, um einen eindeutigen Bezeichner oder [MAPIUID](mapiuid.md)zu registrieren, wenn Ihr Anbieter ein Adressbuch- oder Nachrichtenspeicheranbieter ist.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="bc9f3-123">Transportanbieter registrieren **MAPIUID-Strukturen,** wenn MAPI ihre [IXPLogon::AddressTypes-Methode](ixplogon-addresstypes.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="bc9f3-124">Weitere Informationen zum Registrieren einer **MAPIUID finden** Sie unter [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="bc9f3-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="bc9f3-125">Instanziieren Sie ein Anmeldeobjekt, und geben Sie einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="bc9f3-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="bc9f3-126">S_OK, um eine erfolgreiche Anmeldung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="bc9f3-127">MAPI_E_UNCONFIGURED, dass mindestens eine der Konfigurationseigenschaften nicht verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="bc9f3-128">MAPI_E_USER_CANCEL, dass der Benutzer das Konfigurationsdialogfeld abgebrochen hat, wodurch Konfigurationseigenschaften nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="bc9f3-129">MAPI_E_FAILONEPROVIDER, dass Ihr Anbieter nicht konfiguriert werden konnte, dass MAPI die Verwendung jedoch unabhängig davon zulassen sollte.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="bc9f3-130">Anmeldemethoden sollten diesen Wert zurückgeben, um einen nicht standardmäßigen Fehler zu melden, z. B. wenn der Anbieter ein Kennwort benötigt und den Benutzer nicht dazu aufgefordert werden kann, da die Benutzeroberfläche deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="bc9f3-131">In der vorherigen Aufgabenliste wird eine Mindestimplementierung für eine Dienstanbieteranmeldungsmethode beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="bc9f3-132">Sie können bei Bedarf zusätzliche Funktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="bc9f3-133">Beispielsweise rufen einige Anbieter [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) auf, um die Statustabelle in ihrer Anmeldemethode zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bc9f3-134">Um die beste Leistung bei der Anmeldung zu erzielen, vermeiden Sie den Aufruf von [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) oder [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span><span class="sxs-lookup"><span data-stu-id="bc9f3-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="bc9f3-135">Bevor diese Aufrufe abgeschlossen werden können und die Steuerung der Anmeldemethode zurückgeben kann, muss der MAPI-Spooler gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="bc9f3-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc9f3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc9f3-136">See also</span></span>

- [<span data-ttu-id="bc9f3-137">Starten eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="bc9f3-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

