---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439730"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Eigenschaftenblatt an, mit dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann Diese Methode wird in von MAPI implementierten Statusobjekten nicht unterstützt.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Konfigurationseigenschaftsblatts.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Anzeige des Eigenschaftenblatts steuert. Das folgende Flag kann festgelegt werden:
    
UI_READONLY 
  
> Schlägt vor, dass der Anbieter keine Benutzer zum Ändern von Konfigurationseigenschaften aktivieren sollte. Dieses Flag ist nur ein Vorschlag. sie kann ignoriert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurationseigenschaftsblatt wurde erfolgreich angezeigt.
    
MAPI_E_NO_SUPPORT 
  
> Das status-Objekt unterstützt diese Methode nicht, wie durch das Fehlen des STATUS_SETTINGS_DIALOG-Flag in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) -Eigenschaft angegeben wird.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIStatus::SettingsDialog-Methode** zeigt ein Konfigurationseigenschaftsblatt an. Alle Dienstanbieter sollten die **SettingsDialog-Methode** unterstützen, sie ist jedoch nicht erforderlich. Dienstanbieter können eigene Eigenschaftenblätter implementieren oder die Implementierung verwenden, die in der [IMAPISupport::D oConfigPropsheet-Methode des Supportobjekts bereitgestellt](imapisupport-doconfigpropsheet.md) wird. **DoConfigPropsheet erstellt** ein Eigenschaftenblatt mit Lese-/Schreibzugriff. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Remotetransportanbieter über Einstellungen verfügt, sollte er die folgenden Schritte vornehmen:
  
- Öffnen Sie den Profilabschnitt des Transportanbieters.
    
- Holen Sie sich die Eigenschafteneinstellungen des Transportanbieters aus dem Profil.
    
- Zeigen Sie die Eigenschafteneinstellungen in einem Dialogfeld an.
    
- Wenn das Dialogfeld die Bearbeitung der Eigenschafteneinstellungen zulässt, überprüfen Sie, ob die neuen Einstellungen gültig sind, und speichern Sie sie wieder im Profilabschnitt des Transportanbieters.
    
- Geben S_OK oder Fehlerwerte zurück, die während der vorherigen Schritte zurückgegeben wurden.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können das über **SettingsDialog** angezeigte Eigenschaftenblatt verwenden, um eine Vielzahl von Aufgaben auszuführen, z. B.: 
  
- Geben Sie einen Standardnachrichtenspeicher an.
    
- Geben Sie einen Transportauftrag an.
    
- Geben Sie einen Standard-Adressbuchcontainer für das Browsen an.
    
- Geben Sie eine Suchreihenfolge zum Auflösen mehrdeutiger Namen an.
    
- Geben Sie ein standardmäßiges persönliches Adressbuch an.
    
Dienstanbieter können Je nach Eigenschaft Eigenschaftenblätter implementieren, die schreibgeschützt oder eine Mischung aus Berechtigungen sind. Dienstanbieter können unterschiedliche Berechtigungen für einzelne Eigenschaften implementieren, indem Sie Eigenschaftseinschränkungen festlegen. Der Standardmodus für Eigenschaftenblätter ist Lese-/Schreibzugriff. Sie können schreibgeschützte Eigenschaftenblätter anfordern, indem Sie UI_READONLY in Ihren Aufrufen von **SettingsDialog festlegen.** Dienstanbieter, die schreibgeschützte Eigenschaftenblätter implementieren können, können dies tun. Da einige Dienstanbieter den Standardmodus jedoch nicht außer Kraft setzen können, müssen Sie bereit sein, Eigenschaftenblätter eines der beiden Typen zu behandeln. 
  
Da an diesem Vorgang immer eine Benutzeroberfläche beteiligt ist, sollten nur interaktive Clients **SettingsDialog aufrufen.**
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

