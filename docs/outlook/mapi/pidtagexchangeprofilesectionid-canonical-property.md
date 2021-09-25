---
title: PidTagExchangeProfileSectionId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56c74754850451a6d0a4d437ec852a75d2c0aef6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600099"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>PidTagExchangeProfileSectionId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine dynamisch generierte GUID, die verwendet wird, um ein Konto zu bestimmen, wenn Sie mehrere Microsoft Exchange Server Konten verwenden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Kennung:  <br/> |0x3d150102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Mehrere Exchange-Konten  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen mehrere Exchange-Konten anstelle eines einzelnen Exchange Kontos. Um mehrere Exchange Konten aufzunehmen, wurde das MAPI-Profillayout geändert. In Microsoft Office Outlook 2007 und früher enthielten Profile einen festen Profilabschnitt, der Exchange Einstellungen wie Servername, Benutzername und Offlineordnerdatei (OST) zugeordnet war. Lage. Diese Einstellungen wurden mithilfe eines eindeutigen Bezeichners identifiziert, der **PbGlobalProfileSectionGuid-Eigenschaft.** Der für Exchange Einstellungen verwendete Abschnitt wird als Exchange Abschnitt "Globales Profil" bezeichnet. 
  
Ein fester Profilbereichsspeicherort reicht nicht mehr aus, um mehrere Exchange Konten aufzunehmen. Stattdessen ist für jedes Exchange Konto in Ihrem Profil ein Abschnitt vorhanden, der den Einstellungen für dieses Konto zugeordnet ist. Der neue Abschnitt, der für Exchange Einstellungen verwendet wird, wird durch den eindeutigen Bezeichner **emsmdbUID** identifiziert.
  
Im Abschnitt "Nachrichtendienstprofil" für das Exchange-Konto finden Sie eine Eigenschaft, die eine GUID enthält, die beim Erstellen des Kontos dynamisch generiert wird. Diese GUID wird in der **PidTagExchangeProfileSectionId-Eigenschaft** gespeichert. Nachrichtenspeicher und Adressbuchcontainer machen eine Eigenschaft verfügbar, um zu bestimmen, zu welchem Exchange Konto sie gehören. Auf die in der Nachrichtendiensttabelle zugegriffen werden kann, macht jeder Exchange Dienst diese Eigenschaft verfügbar. 
  
Sie können diese Eigenschaft über einen Aufruf von [IMAPIProp::GetProps](imapiprop-getprops.md) on **PidTagExchangeProfileSectionId** abrufen, nachdem Sie eine der folgenden Schnittstellen abgefragt haben: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Wenn das Objekt nicht mit Exchange verbunden ist, gibt der Aufruf **MAPI_E_NOT_FOUND** zurück.
  
Sie können Container für eine **PidTagExchangeProfileSectionId** beim Anzeigen des Adressbuchs einschränken. Sobald Sie einen geöffneten Container geöffnet haben, können Sie die **emsmdbUID** daraus abfragen. Beachten Sie außerdem Folgendes: Wenn ein Empfänger aus einem Exchange Adressbuch ausgewählt wurde, enthält der Empfänger auch die **PidTagExchangeProfileSectionId** in der Liste der Eigenschaften. 
  
> [!NOTE]
> In den Codebeispielen und Funktionsheadern wird diese GUID als **emsmdbUID** bezeichnet. 
  
Eines der Exchange-Konten wird als Legacykonto Exchange gekennzeichnet. In der Regel ist es das erste Konto, das dem Profil hinzugefügt wurde. Jeder Aufruf zum Öffnen von **pbGlobalProfileSectionGuid** wird an den Exchange globalen Abschnitt des Legacykontos umgeleitet. Die Objektmodellaufrufe, die mit dem Nicht-Legacy-Exchange-Konto interagieren, interagieren auch mit dem Legacy-Exchange Konto. 
  
Der Ältere Exchange Dienst verfügt **über** die Eigenschaft PR_EMSMDB_LEGACY (0x3D18000B), die in der Nachrichtendiensttabelle auf **"true"** festgelegt ist. 
  
Die ältere **EmsmdbUID** ist auch im Abschnitt Outlook globales Profil des Profils als **PidTagExchangeProfileSectionId** gestempelt. Code, der zur Unterstützung mehrerer Exchange Konten geschrieben wurde, muss nicht die ältere **EmsmdbUID** abrufen, da sie je nach Konto, mit dem Ihr Code interagiert, die richtige **emsmdbUID** abrufen sollte.
  
## <a name="see-also"></a>Siehe auch



[Verwenden mehrerer Exchange Konten](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

