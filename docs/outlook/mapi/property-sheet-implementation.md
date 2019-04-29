---
title: Eigenschaftenblatt Implementierung
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
# <a name="property-sheet-implementation"></a>Eigenschaftenblatt Implementierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftenblatt ist ein Dialogfeld zum Anzeigen der Eigenschaften eines Objekts. Die Eigenschaften können schreibgeschützt sein, sodass der Benutzer Sie nur anzeigen oder lesen/schreiben kann, sodass der Benutzer Änderungen vornehmen muss. Ein Eigenschaftenblatt enthält mindestens ein überlappendes untergeordnetes Fenster mit dem Namen pages. Jede Seite enthält Steuerelementfenster zum Festlegen einer Gruppe verwandter Eigenschaften. Benutzer navigieren von Seite zu Seite, indem Sie eine Registerkarte auswählen, die die entsprechende Seite in den Vordergrund des Eigenschaftenblatts einfügt.
  
Dienstanbieter müssen ein Eigenschaftenfenster implementieren, das einen minimalen Satz von Eigenschaften im Zusammenhang mit der Konfiguration im Nachrichtendienst anzeigt. Wenn Sie zulassen, dass diese Eigenschaften des Nachrichtendiensts geändert werden, können Sie entweder Benutzern von Clientanwendungen wie der Systemsteuerung erlauben, die Änderungen vorzunehmen oder die Änderungen programmgesteuert zu implementieren. Die Implementierung von Eigenschaftenblättern zum Anzeigen und Bearbeiten anderer Typen von Eigenschaften ist optional. 
  
In der Regel müssen Sie ein Eigenschaftenblatt in den folgenden Situationen anzeigen:
  
- Wenn ein Client die [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode des Status-Objekts aufruft. 
    
- Wenn MAPI die Anmeldemethode Ihres Anbieterobjekts aufruft.
    
- Wenn MAPI die Einstiegspunktfunktion für den Nachrichtendienst Ihres Anbieters aufruft.
    
Transport Anbieter implementieren auch Eigenschaftenblätter, um Eigenschaften im Zusammenhang mit Nachrichtenoptionen anzuzeigen, und Adressbuchanbieter implementieren Eigenschaftenblätter zum Anzeigen und bearbeiten detaillierter Informationen zu Messaging Benutzern und Verteilerlisten, Erweiterte Suche Kriterien und Vorlagen für die Eingabe neuer Benutzer.
  
Zum Erstellen eines Eigenschaftenblatts können Sie eine der folgenden drei Techniken verwenden:
  
- Wie bei jedem Dialogfeld.
    
- Mithilfe des im Windows SDK bereitgestellten allgemeinen Steuerelements.
    
- Mithilfe einer MAPI-Anzeigetabelle.
    
Anbieter sollten die letzte Option wählen (Erstellen eines Eigenschaftenfensters mithilfe einer Anzeigetabelle). Dies ist die einfachste Option, da die Arbeit mit der Windows-Benutzeroberfläche nicht mehr erforderlich ist. 
  
Gehen Sie folgendermaßen vor, um ein Eigenschaftenblatt zu implementieren, das aus einer Anzeigetabelle für die Eigenschaften des Nachrichtendiensts erstellt wurde:
  
1. Rufen Sie [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) auf, um einen Abschnitt im aktuellen Profil zu öffnen. Führen Sie Ihre [MAPIUID](mapiuid.md) oder NULL aus, um den Profilbereich Ihres Anbieters zu öffnen. 
    
2. Rufen Sie [CreateIProp](createiprop.md) auf, um ein Eigenschaftendaten Objekt zu erstellen. 
    
3. Rufen Sie die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode des profile-Abschnitts auf, um alle Eigenschaften des Bereichs in das Datenobjekt der Eigenschaft zu kopieren. 
    
4. Erstellen Sie eine Anzeigetabelle, indem Sie eine oder mehrere [DTPAGE](dtpage.md) -Strukturen, die die Steuerelemente beschreiben, die im Eigenschaftenfenster angezeigt werden und die [BuildDisplayTable](builddisplaytable.md) -Funktion aufrufen, oder indem Sie benutzerdefinierten Code implementieren. 
    
5. Rufen Sie [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) , um ein Eigenschaftenfenster mit den kopierten Eigenschaften anzuzeigen. Übergeben Sie einen Zeiger auf das Datenobjekt der Eigenschaft als _lpConfigData_ -Parameter und einen Zeiger auf die Anzeigetabelle als _lpDisplayTable_ -Parameter. Wenn Sie den Standardzugriffs Modus für dieses Eigenschaftenblatt außer Kraft setzen möchten, legen Sie das DT_EDITABLE-Flag für jedes Steuerelement in der Anzeigetabelle, das eine schreibgeschützte Eigenschaft darstellt, nicht fest. 
    
6. Wenn alle Änderungen im Eigenschaftenfenster vorgenommen wurden, rufen Sie die **IMAPIProp:: CopyTo** -Methode des Property-Datenobjekts auf, um die geänderten Eigenschaften zurück in den profile-Abschnitt zu kopieren. 
    
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). 
  
Ausführliche Informationen zu Anzeige Tabellen finden Sie unter [Display Table Implementation](display-table-implementation.md). 
  
Informationen zum Implementieren eines Steuerelements finden Sie unter [Control Object Implementation](control-object-implementation.md).
  
Zum Abrufen des Indexes eines Steuerelements, das ein Benutzer in einem Listenfeld Anzeigetabelle auswählt, warten Sie, bis der Benutzer auf **OK** oder über **nehmen**klickt. Zu diesem Zeitpunkt wird der Eintragsbezeichner des ausgewählten Elements zurück in die [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle als Wert der vom **ulPRSetProperty** -Element in der [DTBLLBX](dtbllbx.md) -Struktur angegebenen Eigenschaft geschrieben. 
  
Wenn Sie in der Lage sein müssen, Elemente aus Ihrem Listenfeld hinzuzufügen oder zu entfernen, kann die Verwendung einer Anzeigetabelle und der [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode nicht ausgeführt werden. Erwägen Sie stattdessen die Implementierung eines Eigenschaftenblatts mit der Win32-Eigenschaftenblatt-API, die in der Datei comdlg32. dll enthalten ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

