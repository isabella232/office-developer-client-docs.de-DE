---
title: Verwenden mehrerer Exchange-Konten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329653"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="90216-103">Verwenden mehrerer Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="90216-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="90216-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90216-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90216-105">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen die Integration mit mehreren Exchange-E-Mail-Konten.</span><span class="sxs-lookup"><span data-stu-id="90216-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange e-mail accounts.</span></span> <span data-ttu-id="90216-106">In Outlook 2010 oder Outlook 2013 konnte ein Benutzer zwei Exchange-Konten zum gleichen Profil hinzufügen und dennoch umfangreiche Exchange-Funktionen wie die veröffentlichte globale Adressliste (GAL), die Exchange-Abwesenheitskonfiguration und die Ordnerfreigabe nutzen.</span><span class="sxs-lookup"><span data-stu-id="90216-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="90216-107">Wer mit den MAPI-Profilabschnitten für Microsoft Office Outlook 2007 und früher vertraut ist, weiß, dass Exchange-Einstellungen, wie der E-Mail-Benutzername und der Servername, im festen Exchange Global Profile-Abschnitt, **pbGlobalProfileSectionGuid**, gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="90216-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the e-mail user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="90216-108">In Outlook 2010 und Outlook 2013 benötigt jedes Exchange-Konto einen eigenen Profilabschnitt zum Speichern von Einstellungen, was **pbGlobalProfileSectionGuid** überflüssig macht.</span><span class="sxs-lookup"><span data-stu-id="90216-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="90216-p103">Die Exchange-Einstellungen für Outlook 2010 und Outlook 2013 sind weiterhin im Profil gespeichert, aber pro Profil wird dynamisch ein eindeutiger Bezeichner für den Profilabschnitt zugewiesen, der die Einstellungen enthält. Der Speicherort der Exchange-Einstellungen im Profil wird in der [kanonischen Eigenschaft "PidTagExchangeProfileSectionId"](pidtagexchangeprofilesectionid-canonical-property.md) gespeichert, die sich im Nachrichtendienst-Profilabschnitt des Exchange-Kontos befindet. Diese Eigenschaft finden Sie auch im Profilabschnitt für jeden Anbieter in diesem Nachrichtendienst des Kontos. Der eindeutige Bezeichner wird nicht auf dem Server gespeichert und unterscheidet sich von Profil zu Profil.</span><span class="sxs-lookup"><span data-stu-id="90216-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="90216-p104">Outlook 2010 und Outlook 2013 verwenden **PidTagExchangeProfileSectionId** als eindeutigen Bezeichner, um ein Exchange-Konto anzugeben. Bei dieser Art der Verwendung wird dieser eindeutige Bezeichner **emsmdbUID** genannt. Für einige MAPI- und Outlook-Operationen kann eine **emsmdbUID** erforderlich sein, um anzugeben, welches Exchange-Konto für die Operation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="90216-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="90216-p105">Um mehrere Exchange-Konten zu unterstützen, müssen Sie bestimmte Aufrufe neuer Funktionen in Ihrem Code verwenden. Ersetzen Sie jeden Aufruf, der eine **entryID** und entweder [IAddrBook::OpenEntry](iaddrbook-openentry.md) oder [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) auf [IMailUser : IMAPIProp](imailuserimapiprop.md) und [IDistList : IMAPIContainer](idistlistimapicontainer.md) verwendet, durch eine der folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="90216-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="90216-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="90216-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="90216-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="90216-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="90216-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="90216-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="90216-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="90216-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="90216-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="90216-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="90216-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="90216-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="90216-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="90216-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="90216-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="90216-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="90216-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="90216-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="90216-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="90216-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="90216-128">Legacyunterstützung</span><span class="sxs-lookup"><span data-stu-id="90216-128">Legacy support</span></span>

<span data-ttu-id="90216-p106">Alle MAPI-Clients, die vor der Erstellung dieses neuen **emsmdbUID**-Abschnitts geschrieben wurden, werden weiterhin unterstützt. Diese Clients rufen weiterhin den vorherigen globalen Abschnitt ab (**pbGlobalProfileSectionGuid**). Abfragen nach diesem Profilabschnitt werden an ein bestimmtes Exchange-Konto weitergeleitet, das Legacyanfragen verarbeitet. Das Konto, das die Legacyaufrufe verarbeitet, kann anhand der Nachrichtendiensttabelle und durch Hinzufügen einer Spalte für PR_EMSMDB_LEGACY bestimmt werden. Nur für einen Nachrichtendienst ist diese Einstellung auf "true" festgelegt, und sein **PidTagExchangeProfileSectionId** wird als Legacy-**emsmdbUID** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="90216-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="90216-p107">Konfigurierbare MAPI-Einstellungen wie der Standardspeicher und das Standardkonto haben keinen Einfluss darauf, welches Konto Legacyaufrufe verarbeitet. Das Konto, das die Legacyaufrufe verarbeitet, kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="90216-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="90216-p108">Der **emsmdbUID** des Legacykontos wird in den Outlook Global Profile-Abschnitt kopiert. Wenn diese Eigenschaft nicht vorhanden ist, wird durch Abfragen nach der Nachrichtendiensttabelle ermittelt, welches Konto der Legacyhandler ist, und der Wert im Outlook Global Profile-Abschnitt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90216-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="90216-p109">Um es deutlich zu sagen: Der Outlook Global Profile-Abschnitt unterscheidet sich vom Exchange Global Profile-Abschnitt, und in Outlook 2010 und Outlook 2013 ist der Exchange Global Profile-Abschnitt nicht mehr wirklich global, da Sie mehrere Exchange Konten verwenden können. Der Outlook Global Profile-Abschnitt enthält Eigenschaften über Outlook, wie z. B. den Status des MRU-Ordners oder den Status der globalen Verbindung.</span><span class="sxs-lookup"><span data-stu-id="90216-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="90216-140">Adressbuch-Kontokontexte</span><span class="sxs-lookup"><span data-stu-id="90216-140">Address Book Account Contexts</span></span>

<span data-ttu-id="90216-141">Um Adressen mit mehreren Exchange-Konten korrekt aufzulösen, verwenden Sie die neuen Funktionen, die einen Kontenkontext berücksichtigen, sodass Aufrufe an das Adressbuch das richtige Exchange-Konto durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="90216-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="90216-p110">Einige frühere Adressbuch-APIs sind veraltet, da sie keine vollständige Unterstützung mehrerer Exchange-Konten boten. Dieser Kontokontext ist in der Regel eine **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="90216-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="90216-144">Neben der **emsmdbUID** haben mehrere Exchange-Konten auch eine **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="90216-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="90216-145">Der Wert **emsmdbUID** gibt den Konto-Kontext.</span><span class="sxs-lookup"><span data-stu-id="90216-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="90216-146">Der Wert **emsabpUID** identifiziert eine Exchange-Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="90216-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="90216-p111">Der **emsabpUID**-Wert wird typischerweise bei der Auflösung eines Empfängers verwendet. Wenn Sie einen Empfänger mit [IAddrBook::ResolveName](iaddrbook-resolvename.md) auflösen, enthält eine Exchange-Empfängerzeile die Eigenschaft **PR_AB_PROVIDERS** (0x3D010102), die den **emsabpUID**-Wert enthält. Dieser **emsabpUID**-Wert identifiziert den Exchange-Adressbuchanbieter für den jeweiligen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="90216-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="90216-150">Wenn Sie den **emsabpUID**-Wert für eine bestimmte **emsmdbUID** ermitteln möchten, öffnen Sie den Profilabschnitt für **emsmdbUID**, und rufen Sie die Eigenschaft **PR_EMSABP_USER_UID** (0x0x3D1A0102) ab.</span><span class="sxs-lookup"><span data-stu-id="90216-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="90216-p112">Wenn Sie [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) aufrufen, stellen Sie sicher, dass die Exchange-Empfänger in der Liste, die Sie übergeben, die Eigenschaft **PR_AB_PROVIDERS** mit der **emsabpUID**-Eigenschaft enthalten, die dem Adressbuchanbieter entspricht, zu dem der Empfänger gehört. Der Aufruf von [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) in einer Zeile, die Sie von [IAddrBook::ResolveName](iaddrbook-resolvename.md) erhalten haben, erfordert keine zusätzliche Aktion, aber bestimmter Codes ruft [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) in Zeilen auf, die nur die Eigenschaft **PR_ENTRYID** enthalten. Zeilen in dieser und ähnlichen Situationen sollten sowohl **PR_ENTRYID** als auch **PR_AB_PROVIDERS** enthalten, deren Eigenschaft **PR_AB_PROVIDERS** auf die richtige **emsabpUID** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90216-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="90216-154">Eine einfache Beschreibung des Prozesses zum Auflösen mehrerer Exchange-Konten lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="90216-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="90216-p113">Auf der Grundlage des angegebenen eindeutigen Dienstbezeichners sucht Ihr Code in der Tabelle des Nachrichtenspeichers der **PR_SERVICE_UID**-Eigenschaft, die mit Ihrem Dienstbezeichner übereinstimmt. Von dort aus können Sie den richtigen **PR_MDB_PROVIDER** ermitteln. Diese Zeile enthält den entsprechenden Speicher.</span><span class="sxs-lookup"><span data-stu-id="90216-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="90216-158">Auf der Grundlage der angegebenen **emsmdbUID** sucht Ihr Code in der Nachrichtendiensttabelle nach der Zeile, die die **PidTagExchangeProfileSectionId** enthält, die der **emsmdbUID** übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="90216-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90216-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90216-159">See also</span></span>



[<span data-ttu-id="90216-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="90216-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="90216-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="90216-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="90216-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="90216-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="90216-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="90216-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="90216-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="90216-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="90216-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="90216-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="90216-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="90216-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="90216-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="90216-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="90216-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="90216-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="90216-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="90216-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="90216-170">Kanonische PidTagExchangeProfileSectionId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="90216-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="90216-171">Öffnen des globalen Profilabschnitts</span><span class="sxs-lookup"><span data-stu-id="90216-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

