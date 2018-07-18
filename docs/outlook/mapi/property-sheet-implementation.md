---
title: Implementierung von Eigenschaftenblättern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 406451adac3cd73286feb787bd6b4d2f356aa283
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795325"
---
# <a name="property-sheet-implementation"></a>Implementierung von Eigenschaftenblättern

  
  
**Betrifft**: Outlook 
  
Ein Eigenschaftenblatt wird ein Dialogfeld zum Anzeigen der Eigenschaften eines Objekts. Die Eigenschaften können schreibgeschützt, dem der Benutzer nur Sie können diese anzeigen oder Lese-/Schreibzugriff, sodass der Benutzer Änderungen vornehmen. Ein Eigenschaftenblatt enthält eine oder mehrere überlappende untergeordnete Fenster als Seiten bezeichnet. Jede Seite enthält Steuerelement Windows für eine Gruppe von verwandten Eigenschaften festlegen. Benutzer Navigieren von einer Seite auf durch Auswählen einer Registerkarte, die die entsprechende Seite im Vordergrund im Eigenschaftsfenster bringt.
  
Dienstanbieter müssen ein Eigenschaftenblatt implementieren, die einen minimalen Satz von Eigenschaften im Zusammenhang mit der Konfiguration im Nachrichtendienst angezeigt. Wenn Sie diesen Dienst Nachrichteneigenschaften geändert werden können, können Sie entweder Benutzer des Clients zulassen Anwendungen wie die Systemsteuerung, um die Änderungen vornehmen, oder die Änderungen programmgesteuert implementieren. Implementieren von Eigenschaftenseiten zum Anzeigen und Bearbeiten von anderen Arten von Eigenschaften ist optional. 
  
In der Regel müssen Sie in den folgenden Situationen ein Eigenschaftenfenster anzuzeigen:
  
- Wenn ein Client [SettingsDialog Ihr Status des Objekts](imapistatus-settingsdialog.md) aufruft. 
    
- Wenn MAPI Anbieter-Objekts Logon-Methode aufruft.
    
- Wenn MAPI die Eintrags-Funktion für Messagingdiensts des Anbieters aufruft.
    
Transportanbieter auch implementieren Sie Eigenschaftenseiten, um Eigenschaften im Zusammenhang mit Nachrichtenoptionen anzuzeigen und adressbuchanbietern implementierte Eigenschaft Sheets zum Anzeigen und bearbeiten ausführliche Informationen zu Benutzern und Verteilerlisten, erweiterte Suche messaging Kriterien und Vorlagen für neue Benutzer eingeben.
  
Eines der folgenden drei Verfahren können Sie um ein Eigenschaftenblatt zu erstellen:
  
- Manuell, wie Sie alle im Dialogfeld.
    
- Mithilfe des common Control Blatt-Eigenschaft im Windows SDK bereitgestellt.
    
- Mithilfe von MAPI zeigen Sie Tabelle an.
    
Anbieter sollte die letzte Option wählen (erstellen ein Eigenschaftenblatts mithilfe einer Tabelle anzeigen). Dies ist die einfachste Möglichkeit, da es entfällt die Notwendigkeit der Windows-Benutzeroberfläche entwickelt. 
  
Um ein Eigenschaftenblatt erstellt aus einer Tabelle Anzeige für Ihre Nachricht Diensteigenschaften implementieren möchten, verwenden Sie die folgende Schritte aus:
  
1. Rufen Sie [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) , um einen Abschnitt im aktuellen Profil zu öffnen. Übergeben Sie Ihre [MAPIUID](mapiuid.md) oder NULL, um Ihre Anbieterabschnitt Profil zu öffnen. 
    
2. Rufen Sie [CreateIProp](createiprop.md) um ein Property-Daten-Objekt zu erstellen. 
    
3. Rufen Sie Profilabschnitt [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um alle Eigenschaften des Bereichs in das Eigenschaftenobjekt Daten kopieren. 
    
4. Erstellen Sie eine Anzeige Tabelle erstellen eine oder mehrere [DTPAGE](dtpage.md) -Strukturen, die beschreiben, die Steuerelemente auf dem Eigenschaftenblatt und Aufruf der Funktion [BuildDisplayTable](builddisplaytable.md) angezeigt werden soll, indem oder benutzerdefinierten Code implementieren. 
    
5. Rufen Sie [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) , um einem Eigenschaftenfenster anzuzeigen, die die kopierten Eigenschaften hat. Übergeben Sie einen Zeiger auf die Daten Property-Objekt als Parameter _LpConfigData_ und einen Zeiger auf die Tabelle Anzeige als _LpDisplayTable_ -Parameter. Wenn Sie der Standardzugriffsmodus für dieses Eigenschaftenblatt außer Kraft setzen möchten, legen Sie die DT_EDITABLE-Flag für jedes Steuerelement nicht in der Tabelle anzeigen, die eine schreibgeschützte Eigenschaft darstellt. 
    
6. Wenn alle Änderungen im Eigenschaftenfenster vorgenommen wurden, rufen Sie die Eigenschaft Datenobjekt **IMAPIProp::CopyTo** -Methode, um die geänderten Eigenschaften zurück in den Profilabschnitt zu kopieren. 
    
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). 
  
Ausführliche Informationen zu Tabellen anzeigen finden Sie unter [Tabelle Implementierung anzuzeigen](display-table-implementation.md). 
  
Informationen zum Implementieren eines Steuerelements finden Sie unter [Implementierung der Steuerelement-Objekts](control-object-implementation.md).
  
Um den Index eines Steuerelements abzurufen, die ein Benutzer in einem Listenfeld für Anzeige Tabelle auswählt, warten Sie, bis der Benutzer auf **OK** oder **Übernehmen**klickt. Zu diesem Zeitpunkt die Eintrags-ID des ausgewählten Elements wird in zurückgeschrieben der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle als der Wert der Eigenschaft durch die **UlPRSetProperty** Mitglied in der Struktur [DTBLLBX](dtbllbx.md) angegeben. 
  
Wenn Sie hinzufügen oder Entfernen von Elementen in Ihrem Listenfeld werden müssen, funktioniert mit einer Tabelle anzeigen und die [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) -Methode nicht. Stattdessen Sie Implementieren eines Eigenschaftenblatts mit der Blatt-API in Win32-Eigenschaft, die in der Datei comdlg32.dll enthalten sind. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

