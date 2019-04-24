---
title: Kanonische PidTagExchangeProfileSectionId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316429"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Kanonische PidTagExchangeProfileSectionId-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine dynamisch generierte GUID, mit der ein Konto ermittelt wird, wenn Sie mehrere Microsoft Exchange Server-Konten verwenden.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Kennung:  <br/> |0x3d150102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Mehrere Exchange-Konten  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen mehrere Exchange-Konten anstelle eines einzelnen Exchange-Kontos. Zur Unterstützung mehrerer Exchange-Konten wurde das MAPI-Profil Layout geändert. In Microsoft Office Outlook 2007 und früheren Versionen enthielten Profile einen Abschnitt mit festen Profilen für Exchange-Einstellungen wie Servername, Benutzername und Offline Ordner Datei (Ost). Lage. Diese Einstellungen wurden mithilfe eines eindeutigen Bezeichners, der **pbglobalprofilesectionguidabgerufen** -Eigenschaft, identifiziert. Der für Exchange-Einstellungen verwendete Abschnitt wird als Abschnitt Exchange Global profile bezeichnet. 
  
Ein fester Profil Abschnitts Speicherort ist nicht mehr ausreichend, um mehrere Exchange-Konten aufzunehmen. Stattdessen ist für jedes Exchange-Konto in Ihrem Profil ein Abschnitt vorhanden, der den Einstellungen für dieses Konto zugeordnet ist. Der neue Abschnitt für Exchange-Einstellungen wird durch die eindeutige ID **emsmdbUID**identifiziert.
  
Im Abschnitt Nachrichtendienst Profil für das Exchange-Konto finden Sie eine Eigenschaft, die eine GUID enthält, die zum Zeitpunkt der Erstellung des Kontos dynamisch generiert wird. Diese GUID wird in der **PidTagExchangeProfileSectionId** -Eigenschaft gespeichert. Nachrichtenspeicher und Adressbuchcontainer stellen eine Eigenschaft bereit, um zu bestimmen, zu welchem Exchange-Konto Sie gehören. In der Tabelle Nachrichtendienste verfügbar, macht jeder Exchange-Dienst diese Eigenschaft verfügbar. 
  
Sie können diese Eigenschaft über einen Aufruf von [IMAPIProp::](imapiprop-getprops.md) getpropes auf **PidTagExchangeProfileSectionId** abrufen, nachdem Sie eine der folgenden Schnittstellen abgefragt haben: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Wenn das Objekt nicht mit Exchange verbunden ist, gibt der Aufruf **MAPI_E_NOT_FOUND**zurück.
  
Sie können Container für eine **PidTagExchangeProfileSectionId** einschränken, wenn das Adressbuch angezeigt wird. Sobald Sie über einen geöffneten Container verfügen, können Sie den **emsmdbUID** davon Abfragen. Außerdem sollte beachtet werden, dass ein Empfänger, der aus einem Exchange-Adressbuch ausgewählt wurde, auch die **PidTagExchangeProfileSectionId** in der Liste der Eigenschaften hat. 
  
> [!NOTE]
> In den Codebeispielen und Funktions Kopfzeilen wird diese GUID als **emsmdbUID**bezeichnet. 
  
Eines der Exchange-Konten ist als Legacy-Exchange-Konto gekennzeichnet. NormalerWeise ist es das erste Konto, das dem Profil hinzugefügt wurde. Jeder Aufruf von Open **pbglobalprofilesectionguidabgerufen** wird an den Abschnitt Exchange Global des Legacy Kontos umgeleitet. Die Objektmodellaufrufe, die mit dem Exchange-Konto nicht Legacy interagieren, interagieren auch mit dem Legacy-Exchange-Konto. 
  
Der Exchange-Legacy Dienst hat die Eigenschaft **PR_EMSMDB_LEGACY** (0x3D18000B), die in der Tabelle Nachrichtendienste auf **true** festgelegt ist. 
  
Das Legacy- **emsmdbUID** wird auch im Abschnitt Outlook Global Profile des Profils als **PidTagExchangeProfileSectionId**gestempelt. Code, der zur Unterstützung mehrerer Exchange-Konten geschrieben wurde, sollte nicht den Legacy- **emsmdbUID** abrufen müssen, da er die richtige **emsmdbUID**erhalten soll, je nachdem, mit welchem Konto Ihr Code interagiert.
  
## <a name="see-also"></a>Siehe auch



[Verwenden mehrerer Exchange-Konten](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

