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
ms.openlocfilehash: a40046a26efe118e48cdca4749d2e99212bb8bfe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579843"
---
# <a name="sync"></a>SYNC

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Informationen für die Synchronisierung zwischen einer lokalen Speicher und einem Server gestartet. Diese Informationen werden während der [Synchronisieren Zustand](synchronize-state.md)verwendet.
  
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
  
- [Out] / [in] eine Bitmaske der folgenden Werte, die das Verhalten während der Synchronisation ändert:
    
- UPS_UPLOAD_ONLY
    
  - [in] Der Client wird nur Upload ausgeführt werden. Outlook gibt nur lokal geänderten Ordner zurück.
    
- UPS_DNLOAD_ONLY
    
  - [in] Der Client wird nur Download ausgeführt werden. Outlook sollte nicht hochladen Bits für Ordner deaktivieren.
    
- UPS_THESE_FOLDERS
    
  - [in] Der Client wird eine angegebene Gruppe von Ordnern mit der angegebenen Eintrags-IDs synchronisiert werden. Dieses Kennzeichen können mit der **UPS_UPLOAD_ONLY** oder eine **UPS_DNLOAD_ONLY** kombiniert werden. 
    
- UPS_OK
    
  - [out] Synchronisierung war erfolgreich. Der Client legt dies fest, nach dem Hochladen, oder eine vollständige Synchronisierung abgeschlossen ist.
    
- 
    
    > [!NOTE]
    > Obwohl der Client kann entweder hochladen oder vollständig synchronisieren (hochladen und herunterladen) Ordner und Elemente mit der API Replikation der Client gibt *UlFlags* mit nur einer Richtung der Replikation zu einem Zeitpunkt – die **UPS_UPLOAD_ONLY** oder **UPS_DNLOAD_ONLY** -Flag. Im Fall von eine vollständige Synchronisierung führt der Client zunächst Upload mit dem **UPS_UPLOAD_ONLY** -Flag, und klicken Sie dann einen Download mit dem **UPS_DNLOAD_ONLY** -Flag. 
  
 _pwzPath_
  
- [out] Pfad zu dem lokalen Speicher.
    
 _Reserved1_
  
- Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _Reserved2_
  
- Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 *PEL* 
  
- [in] Dies ist die Liste von Eintrags-IDs der Ordner synchronisieren, wenn **UPS_THESE_FOLDERS** festgelegt wurde. Finden Sie unter mapidefs.h für die Definition des **LPENTRYLIST**Typs. 
    
 _pulFolderOptions_
  
- [in] Dies ist ein Array von Ordneroptionen für entsprechende Ordner im *Pel* , wenn **UPS_THESE_FOLDERS** festgelegt wurde. Diese Ordneroptionen werden verwendet, wenn die während der [Ordner Zustand hochladen](upload-folder-state.md)in *Pel* aufgeführten Ordner hochladen. Weitere Informationen zu Ordneroptionen finden Sie unter **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)

