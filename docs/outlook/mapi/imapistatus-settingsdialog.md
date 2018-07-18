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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 09a14a3cc9f77527c6bc254dc703328f2c9ce9f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792341"
---
# <a name="imapistatussettingsdialog"></a>IMAPIStatus::SettingsDialog

  
  
**Betrifft**: Outlook 
  
Zeigt ein Eigenschaftenfenster, in dem den Benutzer zum Ändern des Dienstanbieters Konfiguration dieser Methode wird nicht in Status-Objekten unterstützt, die MAPI implementiert.
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster im Eigenschaftsfenster Konfiguration.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Anzeige des Eigenschaftenfensters steuert. Das folgende Flag kann festgelegt werden:
    
UI_READONLY 
  
> Impliziert, dass der Anbieter nicht Benutzer Konfigurationseigenschaften ändern kann sollen. Dieses Kennzeichen ist nur ein Vorschlag. Es kann ignoriert werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Eigenschaftenblatt Konfiguration war erfolgreich angezeigt.
    
MAPI_E_NO_SUPPORT 
  
> Das Statusobjekt unterstützt diese Methode nicht, wie ohne das Flag STATUS_SETTINGS_DIALOG in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.
    
## <a name="remarks"></a>Bemerkungen

**Die SettingsDialog** zeigt ein Eigenschaftenblatt Konfiguration. Alle-Dienstanbieter sollte die **SettingsDialog** -Methode unterstützt, aber es ist nicht erforderlich. Dienstanbieter können ihre eigenen Eigenschaftenseiten implementieren oder verwenden Sie die Implementierung [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) -Methode für die des Unterstützungsobjekts bereitgestellt. **DoConfigPropsheet** erstellt ein Eigenschaftenblatt Lese-/Schreibzugriff. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Weist ein remote-Transport-Anbieter auf eine beliebige Einstellung, sollten sie Folgendes:
  
- Öffnen der Adressbuchhierarchie Profilabschnitt.
    
- Rufen Sie das Transportprotokoll eigenschafteneinstellungen des Anbieters aus dem Profil.
    
- Anzeigen von Eigenschaften in einem Dialogfeld.
    
- Das Dialogfeld ermöglicht das Bearbeiten von Eigenschaften, sicher, dass die neuen Einstellungen gültig sind und in der Adressbuchhierarchie Profilabschnitt wieder zu speichern.
    
- Zurückgeben Sie S_OK oder während der vorherigen Schritte zurückgegebenen Fehlerwerte.
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Das angezeigte über **SettingsDialog** Eigenschaftenblatt können Sie eine Vielzahl von Aufgaben wie die folgenden ausführen: 
  
- Geben Sie einen Standard-Nachrichtenspeicher.
    
- Geben Sie eine Transport-Reihenfolge.
    
- Geben Sie eine standardmäßige Adressbuchcontainer zum Durchsuchen.
    
- Geben Sie eine Suche Reihenfolge zum Auflösen von Namen nicht eindeutig.
    
- Geben Sie ein persönliches Standardadressbuch.
    
Dienstanbieter können implementieren, Eigenschaftenseiten, die Lese-/Schreibzugriff, schreibgeschützt sind oder eine Kombination von Berechtigungen, je nach Eigenschaft. Dienstanbieter können unterschiedliche Berechtigungen für einzelne Eigenschaften implementieren, indem Sie Suchkriterien in Eigenschaft festlegen. Der Standardmodus für Eigenschaftenseiten besteht Lese-/Schreibzugriff. Sie können schreibgeschützte Eigenschaft Sheets anfordern, indem Sie das Flag UI_READONLY in Ihre Anrufe **SettingsDialog**festgelegt. Dienstanbieter, die schreibgeschützte Eigenschaft Sheets implementieren können dazu. Allerdings, da einige Dienstanbieter können Sie nicht den Standardmodus überschreiben, müssen Sie auf die Eigenschaftenseiten eines beliebigen Typs vorbereitet sein. 
  
Da eine Benutzeroberfläche immer diesen Vorgang beteiligt ist, sollte nur interaktive Clients **SettingsDialog**aufrufen.
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)
  
[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

