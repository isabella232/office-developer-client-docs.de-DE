---
title: Implementieren einer Dienstanbieteranmeldung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb64f2780530fd30784bf9a9b197bcde205b4a5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792572"
---
# <a name="implementing-service-provider-logon"></a><span data-ttu-id="7a2eb-103">Implementieren einer Dienstanbieteranmeldung</span><span class="sxs-lookup"><span data-stu-id="7a2eb-103">Implementing Service Provider Logon</span></span>

<span data-ttu-id="7a2eb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a2eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a2eb-105">MAPI-Aufrufen eine Methode in Ihrem Anbieterobjekt Beginn des Anmeldevorgangs mithilfe des Mauszeigers, mit dem Sie von Ihrem Eintrag Point-Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-105">MAPI calls a method in your provider object to begin the logon process by using the pointer that you return from your entry point function.</span></span> <span data-ttu-id="7a2eb-106">Die Methode hängt wie folgt auf den Typ des vom-Dienstanbieter:</span><span class="sxs-lookup"><span data-stu-id="7a2eb-106">The method varies as follows, depending on the type of your service provider:</span></span>
  
- <span data-ttu-id="7a2eb-107">[IABProvider::Logon](iabprovider-logon.md) für adressbuchanbietern implementierte</span><span class="sxs-lookup"><span data-stu-id="7a2eb-107">[IABProvider::Logon](iabprovider-logon.md) for address book providers</span></span> 
    
- <span data-ttu-id="7a2eb-108">[IMSProvider::Logon](imsprovider-logon.md) für Nachricht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="7a2eb-108">[IMSProvider::Logon](imsprovider-logon.md) for message store providers</span></span> 
    
- <span data-ttu-id="7a2eb-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) für Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="7a2eb-109">[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) for transport providers</span></span> 
    
<span data-ttu-id="7a2eb-110">Führen Sie die folgenden Aufgaben in jegliches Logon-Methode, die Sie implementieren:</span><span class="sxs-lookup"><span data-stu-id="7a2eb-110">Perform the following tasks in whatever logon method you implement:</span></span>
  
1. <span data-ttu-id="7a2eb-111">Erhöhen Sie die Anzahl der Verweise auf die Support-Objekt, das als Eingabeparameter übergeben wird, durch dessen [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-111">Increment the reference count on the support object that is passed as an input parameter by calling its [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) method.</span></span> 
    
2. <span data-ttu-id="7a2eb-112">Rufen Sie die des Unterstützungsobjekts [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode zum Zugriff auf Ihr Profilabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-112">Call the support object's [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to access your profile section.</span></span> 
    
3. <span data-ttu-id="7a2eb-113">Rufen Sie den Profilabschnitt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die folgenden Eigenschaften festlegen:</span><span class="sxs-lookup"><span data-stu-id="7a2eb-113">Call the profile section's [IMAPIProp::SetProps](imapiprop-setprops.md) method to set the following properties:</span></span> 
    
  - <span data-ttu-id="7a2eb-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a2eb-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
  - <span data-ttu-id="7a2eb-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a2eb-115">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
  - <span data-ttu-id="7a2eb-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a2eb-116">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>
    
  - <span data-ttu-id="7a2eb-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7a2eb-117">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="7a2eb-118">Versuchen Sie nicht den Profil Eigenschaften des Abschnitts **PR_RESOURCE_FLAGS** oder **PR_PROVIDER_DLL_NAME** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-118">Do not attempt to set the profile section's **PR_RESOURCE_FLAGS** or **PR_PROVIDER_DLL_NAME** properties.</span></span> <span data-ttu-id="7a2eb-119">Bei der Anmeldung sind diese Eigenschaften schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-119">At logon time, these properties are read-only.</span></span> 
  
4. <span data-ttu-id="7a2eb-120">Überprüfen Sie, dass die Eigenschaften für die Konfiguration benötigten entweder im Profil gespeichert werden oder vom Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-120">Check that the properties you need for configuration are either stored in the profile or are available from the user.</span></span> <span data-ttu-id="7a2eb-121">Weitere Informationen zum Überprüfen der Konfigurations finden Sie unter [Überprüfen der Dienstkonfiguration Anbieter](verifying-service-provider-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="7a2eb-121">For more information about checking your configuration, see [Verifying Service Provider Configuration](verifying-service-provider-configuration.md).</span></span>
    
5. <span data-ttu-id="7a2eb-122">Rufen Sie die Support-Objekt [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) -Methode, um eine eindeutige Kennung oder [MAPIUID](mapiuid.md), registrieren, wenn der Anbieter einen Address Book oder einer Nachricht-Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-122">Call the support object's [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md), if your provider is an address book or message store provider.</span></span> <span data-ttu-id="7a2eb-123">Transportanbieter registrieren **MAPIUID** Strukturen, wenn MAPI ihre [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-123">Transport providers register **MAPIUID** structures when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="7a2eb-124">Weitere Informationen zum Registrieren einer **MAPIUID**finden Sie unter [Registrieren Service Provider eindeutige Bezeichner](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="7a2eb-124">For more information about registering a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
    
6. <span data-ttu-id="7a2eb-125">Instanziieren Sie ein Objekt Anmeldung und mit einem der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="7a2eb-125">Instantiate a logon object and return with one of the following values:</span></span>
    
  - <span data-ttu-id="7a2eb-126">S_OK erfolgreichen Anmeldung an.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-126">S_OK to indicate a successful logon.</span></span>
    
  - <span data-ttu-id="7a2eb-127">Um anzugeben, dass eine oder mehrere der die Konfigurationseigenschaften MAPI_E_UNCONFIGURED waren nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-127">MAPI_E_UNCONFIGURED to indicate that one or more of the configuration properties were unavailable.</span></span>
    
  - <span data-ttu-id="7a2eb-128">MAPI_E_USER_CANCEL, um anzugeben, dass der Benutzer das Dialogfeld Konfiguration abgebrochen verursacht Konfigurationseigenschaften nicht verfügbar zu sein.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-128">MAPI_E_USER_CANCEL to indicate that the user canceled the configuration dialog box, causing configuration properties to be unavailable.</span></span>
    
  - <span data-ttu-id="7a2eb-129">MAPI_E_FAILONEPROVIDER, um anzugeben, dass der Anbieter nicht konfiguriert werden konnte, aber die MAPI, unabhängig davon verwendet werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-129">MAPI_E_FAILONEPROVIDER to indicate that your provider could not be configured, but that MAPI should allow it to be used regardless.</span></span> <span data-ttu-id="7a2eb-130">Anmeldemethoden sollte diesen Wert, um eine ein nicht schwerwiegender Fehler, beispielsweise wenn der Anbieter ist ein Kennwort erforderlich und kann nicht für sie Benutzer auffordern, da die Benutzeroberfläche deaktiviert ist melden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-130">Logon methods should return this value to report a nonfatal error, such as when the provider requires a password and cannot prompt the user for it because the user interface is disabled.</span></span> 
    
<span data-ttu-id="7a2eb-131">Die obigen Liste der Vorgänge wird eine minimale Implementierung für eine Service Provider Logon-Methode beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-131">The preceding list of tasks describes a minimum implementation for a service provider logon method.</span></span> <span data-ttu-id="7a2eb-132">Sie können zusätzliche Funktionen bei Bedarf einschließen.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-132">You can include additional functionality, if necessary.</span></span> <span data-ttu-id="7a2eb-133">Einige Anbieter rufen beispielsweise [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) zum Aktualisieren der Tabelle "Status" in ihre Logon (Methode).</span><span class="sxs-lookup"><span data-stu-id="7a2eb-133">For example, some providers call [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) to update the status table in their logon method.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7a2eb-134">Um bei der Anmeldung die beste Leistung zu erzielen, vermeiden Sie [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) oder [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-134">To achieve the best performance at logon time, avoid calling either [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) or [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md).</span></span> <span data-ttu-id="7a2eb-135">Bevor dieser Anrufe können und die Steuerung an Ihre Logon (Methode) zurück, muss die MAPI-Warteschlange gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7a2eb-135">Before these calls can complete and return control to your logon method, the MAPI spooler must be started.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a2eb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a2eb-136">See also</span></span>

- [<span data-ttu-id="7a2eb-137">Starten eines Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="7a2eb-137">Starting a Service Provider</span></span>](starting-a-service-provider.md)

