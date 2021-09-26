---
title: Property Sheet-Implementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8037845cce7a3c24f2904a380bbf3fac8c8868a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599228"
---
# <a name="property-sheet-implementation"></a>Property Sheet-Implementierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftenblatt ist ein Dialogfeld zum Anzeigen der Eigenschaften eines Objekts. Die Eigenschaften können schreibgeschützt sein, sodass der Benutzer sie nur anzeigen kann, oder Lese-/Schreibzugriff, sodass der Benutzer Änderungen vornehmen kann. Ein Eigenschaftenblatt enthält ein oder mehrere überlappende untergeordnete Fenster, die als Seiten bezeichnet werden. Jede Seite enthält Steuerelementfenster zum Festlegen einer Gruppe verwandter Eigenschaften. Benutzer navigieren von Seite zu Seite, indem sie eine Registerkarte auswählen, die die entsprechende Seite in den Vordergrund des Eigenschaftenblatts bringt.
  
Dienstanbieter müssen ein Eigenschaftenblatt implementieren, das einen minimalen Satz von Eigenschaften im Zusammenhang mit der Konfiguration im Nachrichtendienst anzeigt. Wenn Sie zulassen, dass diese Nachrichtendiensteigenschaften geändert werden, können Sie benutzern von Clientanwendungen, z. B. der Systemsteuerung, erlauben, die Änderungen vorzunehmen oder die Änderungen programmgesteuert zu implementieren. Das Implementieren von Eigenschaftenblättern zum Anzeigen und Bearbeiten anderer Eigenschaftentypen ist optional. 
  
In der Regel müssen Sie in den folgenden Situationen ein Eigenschaftenblatt anzeigen:
  
- Wenn ein Client die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) ihres Statusobjekts aufruft. 
    
- Wenn MAPI die Anmeldemethode des Anbieterobjekts aufruft.
    
- Wenn die MAPI die Einstiegspunktfunktion für den Nachrichtendienst Ihres Anbieters aufruft.
    
Transportanbieter implementieren auch Eigenschaftenblätter, um Eigenschaften im Zusammenhang mit Nachrichtenoptionen anzuzeigen, und Adressbuchanbieter implementieren Eigenschaftenblätter zum Anzeigen und Bearbeiten detaillierter Informationen zu Messagingbenutzern und Verteilerlisten, erweiterten Suchkriterien und Vorlagen für die Eingabe neuer Benutzer.
  
Sie können eine der folgenden drei Techniken zum Erstellen eines Eigenschaftenblatts verwenden:
  
- Manuell, wie bei jedem Dialogfeld.
    
- Mithilfe des allgemeinen Steuerelements des Eigenschaftenblatts, das im Windows SDK bereitgestellt wird.
    
- Mithilfe einer MAPI-Anzeigetabelle.
    
Anbieter sollten die letzte Option auswählen (erstellen Sie ein Eigenschaftenblatt mithilfe einer Anzeigetabelle). Dies ist die einfachste Option, da es nicht mehr erforderlich ist, mit der Windows Benutzeroberfläche zu arbeiten. 
  
Gehen Sie folgendermaßen vor, um ein Eigenschaftenblatt zu implementieren, das aus einer Anzeigetabelle für die Nachrichtendiensteigenschaften erstellt wurde:
  
1. Rufen Sie [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) auf, um einen Abschnitt im aktuellen Profil zu öffnen. Übergeben Sie [Ihre MAPIUID](mapiuid.md) oder NULL, um den Profilabschnitt Ihres Anbieters zu öffnen. 
    
2. Rufen [Sie CreateIProp](createiprop.md) auf, um ein Eigenschaftsdatenobjekt zu erstellen. 
    
3. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) des Profilabschnitts auf, um alle Eigenschaften des Abschnitts in das Eigenschaftsdatenobjekt zu kopieren. 
    
4. Erstellen Sie eine Anzeigetabelle, indem Sie entweder eine oder mehrere [DTPAGE-Strukturen](dtpage.md) erstellen, die die Steuerelemente beschreiben, die auf dem Eigenschaftenblatt angezeigt werden sollen, und indem Sie die [BuildDisplayTable-Funktion](builddisplaytable.md) aufrufen oder benutzerdefinierten Code implementieren. 
    
5. Rufen Sie [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) auf, um ein Eigenschaftenblatt mit den kopierten Eigenschaften anzuzeigen. Übergeben Sie einen Zeiger auf das Eigenschaftsdatenobjekt als _lpConfigData-Parameter_ und einen Zeiger auf die Anzeigetabelle als _lpDisplayTable-Parameter._ Wenn Sie den Standardzugriffsmodus für dieses Eigenschaftenblatt überschreiben möchten, legen Sie nicht das flag DT_EDITABLE für jedes Steuerelement in der Anzeigetabelle fest, das eine schreibgeschützte Eigenschaft darstellt. 
    
6. Wenn alle Änderungen im Eigenschaftenfenster vorgenommen wurden, rufen Sie die **IMAPIProp::CopyTo-Methode** des Eigenschaftendatenobjekts auf, um die geänderten Eigenschaften zurück in den Profilabschnitt zu kopieren. 
    
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) 
  
Ausführliche Informationen zu Anzeigetabellen finden Sie unter ["Implementierung von Anzeigetabellen".](display-table-implementation.md) 
  
Informationen zum Implementieren eines Steuerelements finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
Um den Index eines Steuerelements abzurufen, das ein Benutzer in einem Listenfeld einer Anzeigetabelle auswählt, warten Sie, bis der Benutzer auf **"OK"** oder **"Übernehmen"** klickt. An diesem Punkt wird der Eintragsbezeichner des ausgewählten Elements zurück in die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) als Wert der Vom **ulPRSetProperty-Element** in der [DTBLLBX-Struktur](dtbllbx.md) angegebenen Eigenschaft geschrieben. 
  
Wenn Sie Elemente zu Ihrem Listenfeld hinzufügen oder entfernen müssen, funktionieren die Verwendung einer Anzeigetabelle und der [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) nicht. Erwägen Sie stattdessen die Implementierung eines Eigenschaftenblatts mit der Win32-Eigenschaftenblatt-API, die in der comdlg32.dll-Datei enthalten ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

