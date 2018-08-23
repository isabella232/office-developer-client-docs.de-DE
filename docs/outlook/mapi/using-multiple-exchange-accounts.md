---
title: Verwenden mehrerer Exchange-Konten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 3fa32b680f5016d4417efdcf62e9bb1f04a51845
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581384"
---
# <a name="using-multiple-exchange-accounts"></a>Verwenden mehrerer Exchange-Konten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen die Integration mit mehreren Exchange-e-Mail-Konten. In Outlook 2010 oder Outlook 2013 kann ein Benutzer zwei Exchange-Konten hinzuf�gen, um das gleiche Profil und genie�en Sie trotzdem umfassende Exchange-Funktionen wie die ver�ffentlichte globale Adressliste (GAL), Exchange Out-of-Office-Konfiguration und Freigabeeinstellungen.
  
Diese mit den MAPI-Profil Abschnitten für Microsoft Office Outlook 2007 vertraut und früher wissen, dass Exchange-Einstellungen, wie die e-Mail-Benutzernamen und den Servernamen, klicken Sie im festen globale Exchange-Profil **PbGlobalProfileSectionGuid**gespeichert sind. Weitere Informationen �ber die globale Exchange-Profils finden Sie unter [Gewusst wie: �ffnen Sie den globalen Profilabschnitt](http://support.microsoft.com/kb/188482). Outlook 2010 und Outlook 2013 ben�tigt jede Exchange-Konto eine eigene Profilabschnitt zum Speichern von Einstellungen, die **pbGlobalProfileSectionGuid** veraltet vornehmen. 
  
Outlook 2010 and Outlook 2013 Exchange settings are still stored in the profile, but a unique identifier for the profile section that contains their settings is dynamically allocated per profile. The location of the Exchange settings in the profile is stored in the [Kanonische PidTagExchangeProfileSectionId-Eigenschaft](pidtagexchangeprofilesectionid-canonical-property.md), which can be found in the message service profile section of the Exchange account. This property can also be found in the profile section for each provider in this message service of the account. The unique identifier is not stored on the server and will be different across profiles.
  
Outlook 2010 und Outlook 2013 verwenden die **PidTagExchangeProfileSectionId** als eindeutiger Bezeichner, um ein Exchange-Konto anzugeben. Wenn auf diese Weise verwendet wird, wird diese eindeutige ID als die **emsmdbUID**bezeichnet. F�r einige Vorg�nge MAPI- und Outlook m�glicherweise ein **emsmdbUID** ben�tigt, um anzugeben, welche Exchange-Konto f�r den Vorgang verwendet werden soll. 
  
In order to support multiple Exchange accounts, you must use some calls to new functions in your code. Replace any call that uses an **entryID** and either [IAddrBook::OpenEntry](iaddrbook-openentry.md) or [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) on [IMailUser: IMAPIProp](imailuserimapiprop.md) and [IDistList: IMAPIContainer](idistlistimapicontainer.md) with one of the following functions. 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>Legacy-Unterst�tzung

MAPI-Clients vor der Erstellung dieses neue **emsmdbUID** Abschnitts geschrieben werden weiterhin unterst�tzt. Diese Clients werden weiterhin der vorherigen globalen Abschnitt **pbGlobalProfileSectionGuid**abgerufen. Abfragen f�r diesen Profilabschnitt werden auf einem bestimmten Exchange-Konto weitergeleitet, die die Vorversion Anfragen behandelt. Das Konto, das die Vorversion Aufrufe behandelt kann in der Tabelle in der Dienste und Hinzuf�gen einer Spalte f�r PR_EMSMDB_LEGACY bestimmt werden. Nur eine Messagingdiensts dies auf True festgelegt, und seine **PidTagExchangeProfileSectionId** wird der Vorversion **emsmdbUID**aufgerufen.
  
> [!NOTE]
> [!HINWEIS] Konfigurierbare MAPI-Einstellungen wie die Standard-Informationsspeichers und das Standardkonto wirken sich nicht auf dem Konto legacy get�tigte Anrufe behandelt werden. Das Konto, das die Vorversion Aufrufe behandelt kann nicht konfiguriert werden. 
  
Die **emsmdbUID** des legacy-Kontos wird in der globalen Profilabschnitt Outlook kopiert. Wenn diese Eigenschaft nicht vorhanden ist, wird f�r die Nachricht Services Tabelle Abfragen bestimmen, welches Konto der Vorversion Handler ist und legen Sie den Wert in der globalen Profilabschnitt Outlook. 
  
Deaktivieren der Outlook sich im Abschnitt globale Profile aus dem Exchange-Abschnitt der globalen Profil unterscheidet und in Outlook 2010 und Outlook 2013 Abschnitts Profile globale Exchange ist nicht mehr wirklich globale m�ssen Sie mehrere Exchange-Konten sein. Die globale Benutzerprofilabschnitt Outlook enth�lt Outlook wie den Status des Ordners MRU oder den Status der Verbindung, globale Eigenschaften.
  
## <a name="address-book-account-contexts"></a>Address Book Konto Kontext

Um Adressen ordnungsgem�� mit mehreren Exchange-Konten zu beheben, verwenden Sie die neuen Funktionen, die einen Konto Kontext ergreifen, damit Anrufe im Adressbuch das richtige Exchange-Konto suchen.
  
Einige fr�here Adressbuch APIs wurden verworfen, da die APIs nicht vollst�ndig mehrere Exchange-f�hig sind. In diesem Kontext ist in der Regel ein **emsmdbUID**.
  
Zus�tzlich zu den **emsmdbUID**haben mehrere Exchange-Konten auch ein **emsabpUID**.
  
1. Der Wert **emsmdbUID** gibt den Konto-Kontext. 
    
2. Der Wert **emsabpUID** identifiziert eine Exchange-Adressbuchanbieter. 
    
The **emsabpUID** value is typically used when resolving a recipient. When resolving a recipient using [IAddrBook::ResolveName](iaddrbook-resolvename.md), an Exchange recipient row contains the **PR_AB_PROVIDERS** (0x3D010102) property, which contains the **emsabpUID** value. This **emsabpUID** value identifies the Exchange address book provider for the specific recipient. 
  
Wenn Sie den Wert **emsabpUID** f�r einen bestimmten **emsmdbUID**ermitteln m�chten, �ffnen Sie den Profilabschnitt f�r die **emsmdbUID**, und rufen Sie die **PR_EMSABP_USER_UID** (0x0x3D1A0102)-Eigenschaft. 
  
If you are calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), make sure that the Exchange recipients in the list that you pass in contain the **PR_AB_PROVIDERS** property that has the **emsabpUID** that corresponds to the address book provider that the recipient belongs to. Calling [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on a row that you obtained from [IAddrBook::ResolveName](iaddrbook-resolvename.md) requires no additional action, but some code will call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) on rows that contain only the **PR_ENTRYID** property. Rows in this and similar situations should contain both **PR_ENTRYID** and **PR_AB_PROVIDERS** with the **PR_AB_PROVIDERS** property set to the correct **emsabpUID**.
  
Eine einfache Beschreibung des Prozesses f�r die Beilegung von mehreren Exchange-Konten lautet wie folgt:
  
- Den eindeutige Bezeichner der Dienst erteilt, sollte der Code in der Tabelle des Nachrichtenspeichers der **PR_SERVICE_UID** -Eigenschaft, die der, die Ihnen �bereinstimmt. Dort k�nnen Sie die richtige **PR_MDB_PROVIDER**bestimmen. Diese Zeile enth�lt den entsprechenden Store.
    
- Ein **emsmdbUID**angegeben, sollte der Code in der Tabelle Nachricht Dienste f�r die Zeile, die die **PidTagExchangeProfileSectionId** verf�gbar macht, die mit der **emsmdbUID**�bereinstimmt.
    
## <a name="see-also"></a>Siehe auch



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[Kanonische PidTagExchangeProfileSectionId-Eigenschaft](pidtagexchangeprofilesectionid-canonical-property.md)


[How To Open the Global Profile Section](http://support.microsoft.com/kb/188482)

