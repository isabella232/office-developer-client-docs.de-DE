---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d38a9930e9bdd3fcc5fb782c5bec45b1b6147e2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567501"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Eigenschaftenblatt an, mit dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann. Diese Methode wird in Statusobjekten, die MAPI implementiert, nicht unterstützt.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des Konfigurationseigenschaftenfensters.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Anzeige des Eigenschaftenblatts steuert. Das folgende Kennzeichen kann festgelegt werden:
    
UI_READONLY 
  
> Schlägt vor, dass der Anbieter Benutzern nicht das Ändern von Konfigurationseigenschaften ermöglichen sollte. Dieses Kennzeichen ist nur ein Vorschlag; sie kann ignoriert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurationseigenschaftenblatt wurde erfolgreich angezeigt.
    
MAPI_E_NO_SUPPORT 
  
> Das Status-Objekt unterstützt diese Methode nicht, wie durch das Fehlen des STATUS_SETTINGS_DIALOG Flags in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) -Eigenschaft angegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIStatus::SettingsDialog-Methode** zeigt ein Konfigurationseigenschaftenblatt an. Alle Dienstanbieter sollten die **SettingsDialog-Methode** unterstützen, ist jedoch nicht erforderlich. Dienstanbieter können eigene Eigenschaftenblätter implementieren oder die in der [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) des Supportobjekts bereitgestellte Implementierung verwenden. **DoConfigPropsheet** erstellt ein Eigenschaftenblatt mit Lese-/Schreibzugriff. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Remote-Transportanbieter Einstellungen hat, sollte er folgendermaßen vorgehen:
  
- Öffnen Sie den Profilabschnitt des Transportanbieters.
    
- Rufen Sie die Eigenschafteneinstellungen des Transportanbieters aus dem Profil ab.
    
- Zeigen Sie die Eigenschafteneinstellungen in einem Dialogfeld an.
    
- Wenn das Dialogfeld das Bearbeiten der Eigenschafteneinstellungen zulässt, überprüfen Sie, ob die neuen Einstellungen gültig sind, und speichern Sie sie wieder im Profilabschnitt des Transportanbieters.
    
- Gibt S_OK oder fehlerwerte zurück, die während der vorherigen Schritte zurückgegeben wurden.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können das über **SettingsDialog** angezeigte Eigenschaftenblatt verwenden, um eine Vielzahl von Aufgaben auszuführen, z. B. die folgenden: 
  
- Geben Sie einen Standardnachrichtenspeicher an.
    
- Geben Sie eine Transportreihenfolge an.
    
- Geben Sie einen Standardadressbuchcontainer für das Browsen an.
    
- Geben Sie eine Suchreihenfolge zum Auflösen von mehrdeutigen Namen an.
    
- Geben Sie ein persönliches Standardadressbuch an.
    
Dienstanbieter können je nach Eigenschaft Eigenschaftenblätter mit Lese-/Schreibzugriff, schreibgeschützt oder einer Mischung aus Berechtigungen implementieren. Dienstanbieter können unterschiedliche Berechtigungen für einzelne Eigenschaften implementieren, indem Sie Eigenschaftseinschränkungen festlegen. Der Standardmodus für Eigenschaftenblätter ist Lese-/Schreibzugriff. Sie können schreibgeschützte Eigenschaftenblätter anfordern, indem Sie das flag UI_READONLY in Ihren Aufrufen von **SettingsDialog** festlegen. Dienstanbieter, die schreibgeschützte Eigenschaftenblätter implementieren können, können dies tun. Da jedoch einige Dienstanbieter den Standardmodus nicht überschreiben können, müssen Sie darauf vorbereitet sein, Eigenschaftenblätter eines der beiden Typen zu verarbeiten. 
  
Da an diesem Vorgang immer eine Benutzeroberfläche beteiligt ist, sollten nur interaktive Clients **SettingsDialog** aufrufen.
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

