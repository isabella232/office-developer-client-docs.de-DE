---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51b9ee138fb26f41ff2df84f7a13432947e9b437
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619659"
---
# <a name="sync"></a>SYNC

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Starten der Synchronisierung zwischen einem lokalen Speicher und einem Server. Diese Informationen werden während des [Synchronisierungsstatus](synchronize-state.md)verwendet.
  
## <a name="quick-info"></a>QuickInfo

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a>Elemente

 _ulFlags_
  
- [out]/[in] Eine Bitmaske der folgenden Flags, die das Verhalten während der Synchronisierung ändert:
    
- UPS_UPLOAD_ONLY
    
  - [in] Der Client führt nur einen Upload durch. Outlook gibt nur lokal geänderte Ordner zurück.
    
- UPS_DNLOAD_ONLY
    
  - [in] Der Client führt nur den Download durch. Outlook sollten Uploadbits für Ordner nicht löschen.
    
- UPS_THESE_FOLDERS
    
  - [in] Der Client synchronisiert einen angegebenen Ordnersatz mit den angegebenen Eintrags-IDs. Dieses Flag kann entweder mit dem **UPS_UPLOAD_ONLY-** oder **UPS_DNLOAD_ONLY** Flag kombiniert werden. 
    
- UPS_OK
    
  - [out] Die Synchronisierung war erfolgreich. Der Client legt dies nach abschluss des Uploads oder einer vollständigen Synchronisierung fest.
    
- 
    
    > [!NOTE]
    > Obwohl der Client Ordner und Elemente mit der Replikations-API entweder hochladen oder vollständig synchronisieren (dann herunterladen) kann, gibt der Client  *ulFlags*  mit jeweils nur einer Richtung der Replikation an – entweder **dem UPS_UPLOAD_ONLY** oder **UPS_DNLOAD_ONLY** Flag. Bei einer vollständigen Synchronisierung führt der Client zuerst einen Upload mit dem **flag UPS_UPLOAD_ONLY** und dann einen Download mit dem **Flag UPS_DNLOAD_ONLY** durch. 
  
 _pwzPath_
  
- [out] Pfad zum lokalen Speicher.
    
 _Reserviert1_
  
- Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _Reserviert2_
  
- Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 *Pel* 
  
- [in] Dies ist die Liste der Eintrags-IDs der Zu synchronisierenden Ordner, wenn **UPS_THESE_FOLDERS** festgelegt wurde. Die Typdefinition von **LPENTRYLIST** finden Sie unter mapidefs.h. 
    
 _pulFolderOptions_
  
- [in] Dies ist ein Array von Ordneroptionen für die entsprechenden Ordner in  *pel,*  wenn **UPS_THESE_FOLDERS** festgelegt wurde. Diese Ordneroptionen werden beim Hochladen der einzelnen Ordner verwendet, die während des [Uploadordnerstatus](upload-folder-state.md)in *pel* aufgeführt sind. Weitere Informationen zu Ordneroptionen finden Sie unter **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)

