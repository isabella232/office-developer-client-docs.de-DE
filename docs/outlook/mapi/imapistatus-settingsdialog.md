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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331542"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Eigenschaftenfenster an, in dem der Benutzer die Konfiguration eines Dienstanbieters ändern kann diese Methode wird in den von MAPI implementierten Statusobjekten nicht unterstützt.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster des Konfigurationseigenschaften Blatts.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Anzeige des Eigenschaftenblatts steuert. Das folgende Flag kann festgelegt werden:
    
UI_READONLY 
  
> Weist darauf hin, dass der Anbieter die Konfigurationseigenschaften nicht ändern sollte. Dieses Flag ist nur ein Vorschlag; Sie kann ignoriert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurationseigenschaften Blatt wurde erfolgreich angezeigt.
    
MAPI_E_NO_SUPPORT 
  
> Das Status-Objekt unterstützt diese Methode nicht, wie durch das Fehlen des STATUS_SETTINGS_DIALOG-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIStatus:: Settingsdialog** -Methode zeigt ein Konfigurationseigenschaften Fenster an. Alle Dienstanbieter sollten die **Settingsdialog** -Methode unterstützen, Sie ist jedoch nicht erforderlich. Dienstanbieter können eigene Eigenschaftenblätter implementieren oder die Implementierung verwenden, die in der [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode des Support-Objekts bereitgestellt wird. **DoConfigPropsheet** erstellt ein Eigenschaftenblatt mit Lese-/Schreibzugriff. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Remote Transportanbieter über Einstellungen verfügt, sollte er folgende Schritte ausführen:
  
- Öffnen Sie den Abschnitt Profil des Transportanbieters.
    
- Rufen Sie die Eigenschafteneinstellungen des Transportanbieters aus dem Profil ab.
    
- Zeigen Sie die Eigenschafteneinstellungen in einem Dialogfeld an.
    
- Wenn im Dialogfeld die Eigenschafteneinstellungen bearbeitet werden können, überprüfen Sie, ob die neuen Einstellungen gültig sind, und speichern Sie Sie im Abschnitt Profil des Transportanbieters.
    
- Zurückgeben von S_OK oder von Fehlerwerten, die während der vorangehenden Schritte zurückgegeben wurden.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Mithilfe des Eigenschaftenblatts, das über **Settingsdialog** angezeigt wird, können Sie verschiedene Aufgaben ausführen, beispielsweise: 
  
- Angeben eines Standardnachrichten Speichers.
    
- Geben Sie einen Transportauftrag an.
    
- Geben Sie einen standardmäßigen Adressbuchcontainer für das Browsen an.
    
- Geben Sie eine Suchreihenfolge zum Auflösen von mehrdeutigen Namen an.
    
- Angeben eines standardmäßigen persönlichen Adressbuchs.
    
Dienstanbieter können abhängig von der Eigenschaft Eigenschaftenblätter implementieren, die Lese-/Schreibzugriff, schreibgeschützt oder eine Kombination aus Berechtigungen sind. Dienstanbieter können unterschiedliche Berechtigungen für einzelne Eigenschaften implementieren, indem Sie Eigenschaftseinschränkungen festlegen. Der Standardmodus für Eigenschaftenblätter ist Lese-/Schreibzugriff. Sie können schreibgeschützte Eigenschaftenblätter anfordern, indem Sie das UI_READONLY-Flag in ihren Aufrufen an **Settingsdialog**festlegen. Dienstanbieter, die schreibgeschützte Eigenschaftenblätter implementieren können, sind in der Lage, dies zu tun. Da einige Dienstanbieter den Standardmodus jedoch nicht außer Kraft setzen können, müssen Sie bereit sein, Eigenschaftenblätter eines der beiden Typen zu behandeln. 
  
Da eine Benutzeroberfläche immer an diesem Vorgang beteiligt ist, sollten nur interaktive Clients **Settingsdialog**aufrufen.
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[Kanonische Pidtagresourcemethods (-Eigenschaft](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

