---
title: Implementierung von Eigenschaftenblatt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430049"
---
# <a name="property-sheet-implementation"></a>Implementierung von Eigenschaftenblatt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftenblatt ist ein Dialogfeld zum Anzeigen der Eigenschaften eines Objekts. Die Eigenschaften können schreibgeschützt sein, sodass der Benutzer sie nur anzeigen oder lesen/schreiben kann, sodass der Benutzer Änderungen vornehmen kann. Ein Eigenschaftenblatt enthält ein oder mehrere überlappende untergeordnete Fenster, die als Seiten bezeichnet werden. Jede Seite enthält Steuerelementfenster zum Festlegen einer Gruppe verwandter Eigenschaften. Benutzer navigieren von Seite zu Seite, indem sie eine Registerkarte auswählen, die die entsprechende Seite in den Vordergrund des Eigenschaftenblatts rückt.
  
Dienstanbieter müssen ein Eigenschaftenblatt implementieren, das einen minimalen Satz von Eigenschaften im Zusammenhang mit der Konfiguration im Nachrichtendienst anzeigt. Wenn Sie zulassen, dass diese Nachrichtendiensteigenschaften geändert werden, können Sie entweder Benutzern von Clientanwendungen, z. B. der Systemsteuerung, erlauben, die Änderungen vorzunehmen oder die Änderungen programmgesteuert zu implementieren. Das Implementieren von Eigenschaftenblättern zum Anzeigen und Bearbeiten anderer Eigenschaftentypen ist optional. 
  
In der Regel müssen Sie in den folgenden Situationen ein Eigenschaftenblatt anzeigen:
  
- Wenn ein Client die [IMAPIStatus::SettingsDialog-Methode des Statusobjekts aufruft.](imapistatus-settingsdialog.md) 
    
- Wenn MAPI die Anmeldemethode des Anbieterobjekts aufruft.
    
- Wenn MAPI die Einstiegspunktfunktion für den Nachrichtendienst Ihres Anbieters aufruft.
    
Transportanbieter implementieren auch Eigenschaftenblätter, um Eigenschaften im Zusammenhang mit Nachrichtenoptionen anzuzeigen, und Adressbuchanbieter implementieren Eigenschaftenblätter, um detaillierte Informationen zu Messagingbenutzern und Verteilerlisten, erweiterten Suchkriterien und Vorlagen für die Eingabe neuer Benutzer anzuzeigen und zu bearbeiten.
  
Sie können eine der folgenden drei Techniken verwenden, um ein Eigenschaftenblatt zu erstellen:
  
- Manuell, wie in einem beliebigen Dialogfeld.
    
- Verwenden Sie das allgemeine Steuerelement des Eigenschaftenblatts im Windows SDK.
    
- Mithilfe einer MAPI-Anzeigetabelle.
    
Anbieter sollten die letzte Option auswählen (Erstellen eines Eigenschaftenblatts mithilfe einer Anzeigetabelle). Dies ist die einfachste Option, da sie die Arbeit mit der Benutzeroberfläche Windows entfällt. 
  
Verwenden Sie das folgende Verfahren, um ein Eigenschaftenblatt zu implementieren, das aus einer Anzeigetabelle für die Nachrichtendiensteigenschaften erstellt wurde:
  
1. Rufen [Sie IMAPISupport::OpenProfileSection auf,](imapisupport-openprofilesection.md) um einen Abschnitt im aktuellen Profil zu öffnen. Übergeben Sie [Ihre MAPIUID](mapiuid.md) oder NULL, um den Profilabschnitt Ihres Anbieters zu öffnen. 
    
2. Rufen [Sie CreateIProp auf,](createiprop.md) um ein Eigenschaftsdatenobjekt zu erstellen. 
    
3. Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) des Profilabschnitts auf, um alle Eigenschaften des Abschnitts in das Eigenschaftsdatenobjekt zu kopieren. 
    
4. Erstellen Sie eine Anzeigetabelle, indem Sie eine oder mehrere [DTPAGE-Strukturen](dtpage.md) erstellen, die die Steuerelemente beschreiben, die auf dem Eigenschaftenblatt angezeigt werden sollen, und indem Sie die [BuildDisplayTable-Funktion](builddisplaytable.md) aufrufen oder benutzerdefinierten Code implementieren. 
    
5. Rufen [Sie IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) auf, um ein Eigenschaftenblatt mit den kopierten Eigenschaften anzeigen zu können. Übergeben Sie einen Zeiger auf das Eigenschaftsdatenobjekt als _lpConfigData-Parameter_ und einen Zeiger auf die Anzeigetabelle als _lpDisplayTable-Parameter._ Wenn Sie den Standardzugriffsmodus für dieses Eigenschaftenblatt außer Kraft setzen möchten, legen Sie nicht das DT_EDITABLE-Flag für jedes Steuerelement in der Anzeigetabelle fest, das eine schreibgeschützte Eigenschaft darstellt. 
    
6. Wenn alle Änderungen im Eigenschaftenblatt vorgenommen wurden, rufen Sie die **IMAPIProp::CopyTo-Methode** des Eigenschaftendatenobjekts auf, um die geänderten Eigenschaften zurück in den Profilabschnitt zu kopieren. 
    
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). 
  
Ausführliche Informationen zu Anzeigetabellen finden Sie unter [Display Table Implementation](display-table-implementation.md). 
  
Informationen zum Implementieren eines Steuerelements finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
Warten Sie, bis der Benutzer auf **OK** oder Anwenden klickt, um den Index eines Steuerelements abzurufen, das ein Benutzer in einem Listenfeld der Anzeigetabelle **auswählt.** An diesem Punkt wird der Eintragsbezeichner des ausgewählten Elements zurück in die [IMAPIProp : IUnknown-Schnittstelle als](imapipropiunknown.md) Wert der Eigenschaft geschrieben, die vom **ulPRSetProperty-Element** in der [DTBLLBX-Struktur](dtbllbx.md) angegeben wird. 
  
Wenn Sie Elemente aus Dem Listenfeld hinzufügen oder entfernen müssen, funktioniert die Verwendung einer Anzeigetabelle und der [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) nicht. Erwägen Sie stattdessen die Implementierung eines Eigenschaftenblatts mit der Win32-Eigenschaftenblatt-API, die in der comdlg32.dll ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

