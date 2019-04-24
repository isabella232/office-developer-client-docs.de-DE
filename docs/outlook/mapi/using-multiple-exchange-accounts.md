---
title: Verwenden mehrerer Exchange-Konten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: a5792ebaf78d77924bc3157be63d937b66e9f4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329653"
---
# <a name="using-multiple-exchange-accounts"></a><span data-ttu-id="981a5-103">Verwenden mehrerer Exchange-Konten</span><span class="sxs-lookup"><span data-stu-id="981a5-103">Using Multiple Exchange Accounts</span></span>

  
  
<span data-ttu-id="981a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="981a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="981a5-105">Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen die Integration in mehrere Exchange-e-Mail-Konten.</span><span class="sxs-lookup"><span data-stu-id="981a5-105">Microsoft Outlook 2010 and Microsoft Outlook 2013 support integration with multiple exchange email accounts.</span></span> <span data-ttu-id="981a5-106">In Outlook 2010 oder Outlook 2013 kann ein Benutzer zwei Exchange-Konten hinzuf�gen, um das gleiche Profil und genie�en Sie trotzdem umfassende Exchange-Funktionen wie die ver�ffentlichte globale Adressliste (GAL), Exchange Out-of-Office-Konfiguration und Freigabeeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="981a5-106">In Outlook 2010 or Outlook 2013, a user could add two exchange accounts to the same profile and still enjoy rich Exchange features such as the published global address list (GAL), Exchange Out-of-Office configuration, and folder sharing.</span></span>
  
<span data-ttu-id="981a5-107">Diejenigen, die mit den MAPI-Profil Abschnitten für Microsoft Office Outlook 2007 und früher vertraut sind, wissen, dass Exchange-Einstellungen, wie beispielsweise der e-Mail-Benutzername und der Servername, im Abschnitt fester Exchange-globaler Profil **pbglobalprofilesectionguidabgerufen**gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="981a5-107">Those familiar with the MAPI profile sections for Microsoft Office Outlook 2007 and earlier know that Exchange settings, such as the email user name and server name, are stored in the fixed Exchange Global Profile section, **pbGlobalProfileSectionGuid**.</span></span> <span data-ttu-id="981a5-108">Outlook 2010 und Outlook 2013 ben�tigt jede Exchange-Konto eine eigene Profilabschnitt zum Speichern von Einstellungen, die **pbGlobalProfileSectionGuid** veraltet vornehmen.</span><span class="sxs-lookup"><span data-stu-id="981a5-108">In Outlook 2010 and Outlook 2013, each Exchange account needs its own profile section to store settings, making the **pbGlobalProfileSectionGuid** obsolete.</span></span> 
  
<span data-ttu-id="981a5-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [Kanonische PidTagExchangeProfileSectionId-Eigenschaft](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span><span class="sxs-lookup"><span data-stu-id="981a5-p103">Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [PidTagExchangeProfileSectionId Canonical Property](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.</span></span>
  
<span data-ttu-id="981a5-p104">Outlook 2010 und Outlook 2013 verwenden die **PidTagExchangeProfileSectionId** als eindeutiger Bezeichner, um ein Exchange-Konto anzugeben. Wenn auf diese Weise verwendet wird, wird diese eindeutige ID als die **emsmdbUID**bezeichnet. F�r einige Vorg�nge MAPI- und Outlook m�glicherweise ein **emsmdbUID** ben�tigt, um anzugeben, welche Exchange-Konto f�r den Vorgang verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="981a5-p104">Outlook 2010 and Outlook 2013 use the **PidTagExchangeProfileSectionId** as a unique identifier to specify an Exchange account. When used in this manner, this unique identifier is known as the **emsmdbUID**. For some MAPI and Outlook operations, an **emsmdbUID** might be required to specify which Exchange account should be used for the operation.</span></span> 
  
<span data-ttu-id="981a5-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser: IMAPIProp](imailuserimapiprop.md) and [IDistList: IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span><span class="sxs-lookup"><span data-stu-id="981a5-p105">In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser : IMAPIProp](imailuserimapiprop.md) and [IDistList : IMAPIContainer](idistlistimapicontainer.md) with one of the following functions.</span></span> 
  
- [<span data-ttu-id="981a5-118">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="981a5-118">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
    
- [<span data-ttu-id="981a5-119">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="981a5-119">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
    
- [<span data-ttu-id="981a5-120">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="981a5-120">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
    
- [<span data-ttu-id="981a5-121">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="981a5-121">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
    
- [<span data-ttu-id="981a5-122">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="981a5-122">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
    
- [<span data-ttu-id="981a5-123">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="981a5-123">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
    
- [<span data-ttu-id="981a5-124">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="981a5-124">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
    
- [<span data-ttu-id="981a5-125">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="981a5-125">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
    
- [<span data-ttu-id="981a5-126">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="981a5-126">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
    
- [<span data-ttu-id="981a5-127">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="981a5-127">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a><span data-ttu-id="981a5-128">Legacy-Unterst�tzung</span><span class="sxs-lookup"><span data-stu-id="981a5-128">Legacy support</span></span>

<span data-ttu-id="981a5-p106">MAPI-Clients vor der Erstellung dieses neue **emsmdbUID** Abschnitts geschrieben werden weiterhin unterst�tzt. Diese Clients werden weiterhin der vorherigen globalen Abschnitt **pbGlobalProfileSectionGuid**abgerufen. Abfragen f�r diesen Profilabschnitt werden auf einem bestimmten Exchange-Konto weitergeleitet, die die Vorversion Anfragen behandelt. Das Konto, das die Vorversion Aufrufe behandelt kann in der Tabelle in der Dienste und Hinzuf�gen einer Spalte f�r PR_EMSMDB_LEGACY bestimmt werden. Nur eine Messagingdiensts dies auf True festgelegt, und seine **PidTagExchangeProfileSectionId** wird der Vorversion **emsmdbUID**aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="981a5-p106">Any MAPI clients written before the creation of this new **emsmdbUID** section are still supported. These clients will continue to retrieve the previous global section, **pbGlobalProfileSectionGuid**. Queries for this profile section will be redirected to one designated Exchange account that handles legacy inquiries. The account that handles the legacy calls can be determined by looking at the message service table and adding a column for PR_EMSMDB_LEGACY. Only one message service will have this set to true, and its **PidTagExchangeProfileSectionId** is called the legacy **emsmdbUID**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="981a5-p107">[!HINWEIS] Konfigurierbare MAPI-Einstellungen wie die Standard-Informationsspeichers und das Standardkonto wirken sich nicht auf dem Konto legacy get�tigte Anrufe behandelt werden. Das Konto, das die Vorversion Aufrufe behandelt kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="981a5-p107">Configurable MAPI settings such as the default store and the default account have no effect on which account handles legacy calls. The account that handles the legacy calls cannot be configured.</span></span> 
  
<span data-ttu-id="981a5-p108">Die **emsmdbUID** des legacy-Kontos wird in der globalen Profilabschnitt Outlook kopiert. Wenn diese Eigenschaft nicht vorhanden ist, wird f�r die Nachricht Services Tabelle Abfragen bestimmen, welches Konto der Vorversion Handler ist und legen Sie den Wert in der globalen Profilabschnitt Outlook.</span><span class="sxs-lookup"><span data-stu-id="981a5-p108">The **emsmdbUID** of the legacy account is copied to the Outlook Global Profile Section. If this property does not exist, querying for the message services table will determine what account is the legacy handler and set the value in the Outlook Global Profile Section.</span></span> 
  
<span data-ttu-id="981a5-p109">Deaktivieren der Outlook sich im Abschnitt globale Profile aus dem Exchange-Abschnitt der globalen Profil unterscheidet und in Outlook 2010 und Outlook 2013 Abschnitts Profile globale Exchange ist nicht mehr wirklich globale m�ssen Sie mehrere Exchange-Konten sein. Die globale Benutzerprofilabschnitt Outlook enth�lt Outlook wie den Status des Ordners MRU oder den Status der Verbindung, globale Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="981a5-p109">To be clear, the Outlook Global Profile Section differs from the Exchange Global Profile Section, and in Outlook 2010 and Outlook 2013 the Exchange Global Profile Section is no longer really global because you can have multiple Exchange accounts. The Outlook Global Profile section contains properties about Outlook, such as the state of the folder MRU or the state of the global connection.</span></span>
  
## <a name="address-book-account-contexts"></a><span data-ttu-id="981a5-140">Address Book Konto Kontext</span><span class="sxs-lookup"><span data-stu-id="981a5-140">Address Book Account Contexts</span></span>

<span data-ttu-id="981a5-141">Um Adressen ordnungsgem�� mit mehreren Exchange-Konten zu beheben, verwenden Sie die neuen Funktionen, die einen Konto Kontext ergreifen, damit Anrufe im Adressbuch das richtige Exchange-Konto suchen.</span><span class="sxs-lookup"><span data-stu-id="981a5-141">To resolve addresses correctly with multiple Exchange accounts, use the new functions that take an account context so that calls to the address book search the correct Exchange account.</span></span>
  
<span data-ttu-id="981a5-p110">Einige fr�here Adressbuch APIs wurden verworfen, da die APIs nicht vollst�ndig mehrere Exchange-f�hig sind. In diesem Kontext ist in der Regel ein **emsmdbUID**.</span><span class="sxs-lookup"><span data-stu-id="981a5-p110">Some previous address book APIs were deprecated because the APIs were not fully multiple Exchange capable. This account context is usually an **emsmdbUID**.</span></span>
  
<span data-ttu-id="981a5-144">Zus�tzlich zu den **emsmdbUID**haben mehrere Exchange-Konten auch ein **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="981a5-144">In addition to the **emsmdbUID**, multiple Exchange accounts also have an **emsabpUID**.</span></span>
  
1. <span data-ttu-id="981a5-145">Der Wert **emsmdbUID** gibt den Konto-Kontext.</span><span class="sxs-lookup"><span data-stu-id="981a5-145">The **emsmdbUID** value identifies the account context.</span></span> 
    
2. <span data-ttu-id="981a5-146">Der Wert **emsabpUID** identifiziert eine Exchange-Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="981a5-146">The **emsabpUID** value identifies an Exchange address book provider.</span></span> 
    
<span data-ttu-id="981a5-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span><span class="sxs-lookup"><span data-stu-id="981a5-p111">The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient.</span></span> 
  
<span data-ttu-id="981a5-150">Wenn Sie den Wert **emsabpUID** f�r einen bestimmten **emsmdbUID**ermitteln m�chten, �ffnen Sie den Profilabschnitt f�r die **emsmdbUID**, und rufen Sie die **PR_EMSABP_USER_UID** (0x0x3D1A0102)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="981a5-150">If you want to determine the **emsabpUID** value for a particular **emsmdbUID**, open up the profile section for the **emsmdbUID** and get the **PR_EMSABP_USER_UID** (0x0x3D1A0102) property.</span></span> 
  
<span data-ttu-id="981a5-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span><span class="sxs-lookup"><span data-stu-id="981a5-p112">If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.</span></span>
  
<span data-ttu-id="981a5-154">Eine einfache Beschreibung des Prozesses f�r die Beilegung von mehreren Exchange-Konten lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="981a5-154">A simple description of the process for resolving multiple Exchange accounts is as follows:</span></span>
  
- <span data-ttu-id="981a5-p113">Den eindeutige Bezeichner der Dienst erteilt, sollte der Code in der Tabelle des Nachrichtenspeichers der **PR_SERVICE_UID** -Eigenschaft, die der, die Ihnen �bereinstimmt. Dort k�nnen Sie die richtige **PR_MDB_PROVIDER**bestimmen. Diese Zeile enth�lt den entsprechenden Store.</span><span class="sxs-lookup"><span data-stu-id="981a5-p113">Given the service unique identifier, your code looks in the table of the message store of the **PR_SERVICE_UID** property that matches the one that you have. From there, you can determine the correct **PR_MDB_PROVIDER**. This row contains the appropriate store.</span></span>
    
- <span data-ttu-id="981a5-158">Ein **emsmdbUID**angegeben, sollte der Code in der Tabelle Nachricht Dienste f�r die Zeile, die die **PidTagExchangeProfileSectionId** verf�gbar macht, die mit der **emsmdbUID**�bereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="981a5-158">Given an **emsmdbUID**, your code looks in the message services table for the row that exposes the **PidTagExchangeProfileSectionId** that matches the **emsmdbUID**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="981a5-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="981a5-159">See also</span></span>



[<span data-ttu-id="981a5-160">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="981a5-160">HrCompareABEntryIDsWithExchangeContext</span></span>](hrcompareabentryidswithexchangecontext.md)
  
[<span data-ttu-id="981a5-161">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="981a5-161">HrDoABDetailsWithExchangeContext</span></span>](hrdoabdetailswithexchangecontext.md)
  
[<span data-ttu-id="981a5-162">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="981a5-162">HrDoABDetailsWithProviderUID</span></span>](hrdoabdetailswithprovideruid.md)
  
[<span data-ttu-id="981a5-163">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="981a5-163">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)
  
[<span data-ttu-id="981a5-164">HrOpenABEntryUsingDefaultContext</span><span class="sxs-lookup"><span data-stu-id="981a5-164">HrOpenABEntryUsingDefaultContext</span></span>](hropenabentryusingdefaultcontext.md)
  
[<span data-ttu-id="981a5-165">HrOpenABEntryWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="981a5-165">HrOpenABEntryWithExchangeContext</span></span>](hropenabentrywithexchangecontext.md)
  
[<span data-ttu-id="981a5-166">HrOpenABEntryWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="981a5-166">HrOpenABEntryWithProviderUID</span></span>](hropenabentrywithprovideruid.md)
  
[<span data-ttu-id="981a5-167">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="981a5-167">HrOpenABEntryWithProviderUIDSupport</span></span>](hropenabentrywithprovideruidsupport.md)
  
[<span data-ttu-id="981a5-168">HrOpenABEntryWithResolvedRow</span><span class="sxs-lookup"><span data-stu-id="981a5-168">HrOpenABEntryWithResolvedRow</span></span>](hropenabentrywithresolvedrow.md)
  
[<span data-ttu-id="981a5-169">HrOpenABEntryWithSupport</span><span class="sxs-lookup"><span data-stu-id="981a5-169">HrOpenABEntryWithSupport</span></span>](hropenabentrywithsupport.md)
  
[<span data-ttu-id="981a5-170">Kanonische PidTagExchangeProfileSectionId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="981a5-170">PidTagExchangeProfileSectionId Canonical Property</span></span>](pidtagexchangeprofilesectionid-canonical-property.md)


[<span data-ttu-id="981a5-171">How To Open the Global Profile Section</span><span class="sxs-lookup"><span data-stu-id="981a5-171">How To Open the Global Profile Section</span></span>](https://support.microsoft.com/kb/188482)

