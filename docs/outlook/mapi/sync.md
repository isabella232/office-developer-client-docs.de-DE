---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433808"
---
# <a name="sync"></a>SYNC

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Informationen zum Starten der Synchronisierung zwischen einem lokalen Speicher und einem Server. Diese Informationen werden während des [Synchronisierungsstatus verwendet.](synchronize-state.md)
  
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
  
- [out]/[in] Eine Bitmaske der folgenden Flags, die das Verhalten während der Synchronisierung ändern:
    
- UPS_UPLOAD_ONLY
    
  - [in] Der Client wird nur hochladen. Outlook gibt nur lokal geänderte Ordner zurück.
    
- UPS_DNLOAD_ONLY
    
  - [in] Der Client wird nur herunterladen ausgeführt. Outlook sollten keine Uploadbits für Ordner löschen.
    
- UPS_THESE_FOLDERS
    
  - [in] Der Client synchronisiert einen angegebenen Satz von Ordnern mit den bereitgestellten Eintrags-IDs. Dieses Flag kann entweder mit dem UPS_UPLOAD_ONLY **oder** **UPS_DNLOAD_ONLY** kombiniert werden. 
    
- UPS_OK
    
  - [out] Die Synchronisierung war erfolgreich. Der Client legt dies nach dem Hochladen fest, oder eine vollständige Synchronisierung ist abgeschlossen.
    
- 
    
    > [!NOTE]
    > Auch wenn der Client Ordner und Elemente entweder mit der Replikations-API hochladen oder vollständig mit der Replikations-API synchronisieren (hochladen und dann herunterladen) kann, gibt der Client *ulFlags* mit nur einer Richtung der Replikation gleichzeitig an – entweder das **flag UPS_UPLOAD_ONLY** oder **UPS_DNLOAD_ONLY.** Bei einer vollständigen Synchronisierung führt der Client  zunächst einen Upload mit dem UPS_UPLOAD_ONLY und dann einen Download mit dem UPS_DNLOAD_ONLY **aus.** 
  
 _pwzPath_
  
- [out] Pfad zum lokalen Speicher.
    
 _Reserved1_
  
- Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _Reserved2_
  
- Dieses Mitglied ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 *pel* 
  
- [in] Dies ist die Liste der Eintrags-IDs der Ordner, die synchronisiert werden sollen, **UPS_THESE_FOLDERS** festgelegt wurde. Die Typdefinition von **LPENTRYLIST** finden Sie unter mapidefs.h. 
    
 _pulFolderOptions_
  
- [in] Dies ist ein Array von Ordneroptionen für entsprechende Ordner in  *Pel,* **wenn UPS_THESE_FOLDERS** festgelegt wurde. Diese Ordneroptionen werden beim Hochladen der einzelnen Ordner verwendet, die in *pel* während des [Status des Uploadordners aufgeführt sind.](upload-folder-state.md) Weitere Informationen zu Ordneroptionen finden Sie unter **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)

