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
  
- [out]/[in] eine Bitmaske der folgenden Flags, die das Verhalten während der Synchronisierung ändert:
    
- UPS_UPLOAD_ONLY
    
  - in Der Client führt nur einen Upload aus. Outlook gibt nur lokal geänderte Ordner zurück.
    
- UPS_DNLOAD_ONLY
    
  - in Der Client führt nur den Download aus. Outlook sollte nicht löschen Bits für Ordner hochladen.
    
- UPS_THESE_FOLDERS
    
  - in Der Client synchronisiert eine angegebene Gruppe von Ordnern mit den bereitgestellten Eintrags-IDs. Dieses Flag kann mit dem **UPS_UPLOAD_ONLY** -oder **UPS_DNLOAD_ONLY** -Flag kombiniert werden. 
    
- UPS_OK
    
  - Out Die Synchronisierung war erfolgreich. Der Client legt dies nach dem Hochladen fest, oder eine vollständige Synchronisierung wird abgeschlossen.
    
- 
    
    > [!NOTE]
    > Auch wenn der Client die Ordner und Elemente mit der Replikations-API entweder hoch-oder vollständig synchronisieren kann (Uploads dann herunterzuladen), gibt der Client *ulFlags* nur mit einer Richtung der Replikation an – entweder der **UPS_UPLOAD_ONLY** oder **UPS_DNLOAD_ONLY** -Flag. Bei einer vollständigen Synchronisierung führt der Client zunächst einen Upload mit dem **UPS_UPLOAD_ONLY** -Flag und dann einen Download mit dem **UPS_DNLOAD_ONLY** -Flag aus. 
  
 _pwzPath_
  
- Out Pfad zum lokalen Speicher.
    
 _Reserved1_
  
- Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 _Reserved2_
  
- Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.
    
 *PEL* 
  
- in Dies ist die Liste der Eintrags-IDs der Ordner, die synchronisiert werden sollen, wenn **UPS_THESE_FOLDERS** festgelegt wurde. Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPENTRYLIST**. 
    
 _pulFolderOptions_
  
- in Dies ist ein Array von Ordneroptionen für entsprechende Ordner in *PEL* , wenn **UPS_THESE_FOLDERS** festgelegt wurde. Diese Ordneroptionen werden beim Hochladen aller in *PEL* aufgeführten Ordner während des [Upload-Ordner Status](upload-folder-state.md)verwendet. Weitere Informationen zu Ordneroptionen finden Sie unter **[UPFLD](upfld.md)**. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[MAPI-Konstanten](mapi-constants.md)

