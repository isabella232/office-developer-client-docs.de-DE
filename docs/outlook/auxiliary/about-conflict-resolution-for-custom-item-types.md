---
title: Informationen zur Konfliktbehebung für benutzerdefinierte Typen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: In diesem Thema wird beschrieben, wie Sie Konflikte für benutzerdefinierte Elementtypen lösen, die Sie in Outlook erstellen.
ms.openlocfilehash: b134d1fcd48cf1274642798f880af5464b8a8ad0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580440"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Informationen zur Konfliktbehebung für benutzerdefinierte Typen

In diesem Thema wird beschrieben, wie Sie Konflikte für benutzerdefinierte Elementtypen lösen, die Sie in Outlook erstellen.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Konfliktlösung für standard Outlook Elementtypen

In Outlook treten Konflikte auf, wenn zwei oder mehr Kopien desselben Elements unabhängig voneinander geändert wurden. Outlook erkennt Konflikte während der Synchronisierung. Beispielsweise können Sie ein Besprechungselement online in Outlook Web App aktualisieren und dann dasselbe Besprechungselement in Outlook aktualisieren, wenn Sie offline arbeiten. Wenn Outlook wieder online geht und die Daten zwischen dem Clientcomputer und dem Server synchronisiert, erkennt es, dass zwei verschiedene Kopien desselben Besprechungselements vorhanden sind.
  
Wenn Outlook Elemente synchronisiert, die zu einem Standardmäßigen Outlook Elementtyp gehören, werden die für diesen Elementtyp spezifischen Eigenschaften berücksichtigt, um mögliche Konflikte zu erkennen. Outlook versucht, Konflikte zu lösen, und speichert die resultierende Kopie im entsprechenden Ordner, ohne dass ein Benutzereingriff angefordert wird. In Fällen, in denen Outlook der Ansicht sind, dass die resultierende Kopie möglicherweise nicht alle wesentlichen Daten enthält, speichert Outlook die konflikteigen Kopien im Ordner "Konflikte" im Ordner "Synchronisierungsprobleme". 
  
> [!NOTE]
> Synchronisierungsprobleme und die zugehörigen Unterordner werden ausgeblendet, bis Sie im Navigationsbereich auf **"Ordnerliste"** klicken. 
  
In solchen Fällen können Benutzer zum Ordner "Konflikte" wechseln, um zu überprüfen, welche Elemente in Konflikt waren, und ob eine Kopie im Ordner "Konflikte" verwendet werden soll, um die Kopie zu ersetzen, die Outlook beibehalten haben.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Konfliktlösung für benutzerdefinierte Elementtypen

### <a name="item-types-and-message-classes"></a>Elementtypen und Meldungsklassen
  
Alle Elemente in Outlook sind einer Nachrichtenklasse zugeordnet. Ein E-Mail-Element ist beispielsweise standardmäßig der Nachrichtenklasse **IPM zugeordnet. Hinweis**. Die Nachrichtenklasse wird in erster Linie verwendet, um das Formular zu identifizieren, das zum Anzeigen des Elements in Outlook verwendet werden soll. Outlook unterstützt eine Liste von Nachrichtenklassen, die den Typen von Elementen zugeordnet sind, die in Outlook integriert sind. Weitere Informationen zu Nachrichtenklassen finden Sie unter [Elementtypen und Meldungsklassen](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Benutzer können benutzerdefinierte Elementtypen erstellen, den benutzerdefinierten Elementtypen benutzerdefinierte Nachrichtenklassen zuweisen und Outlook ein benutzerdefiniertes Formular verwenden, um die benutzerdefinierten Elementtypen anzuzeigen. Sie können z. B. Outlook ein benutzerdefiniertes Geschäftskontaktformular für Ihre Geschäftskontakte anzeigen. Dazu können Sie eine benutzerdefinierte Nachrichtenklasse **IPM erstellen. Contact.Business**, erstellen Sie ein benutzerdefiniertes Formular für diese Nachrichtenklasse, und weisen Sie Geschäftskontakte mit dieser Nachrichtenklasse zu. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registrieren eines Konfliktlösungsschemas für benutzerdefinierte Elementtypen
  
Wenn Sie einen benutzerdefinierten Elementtyp erstellen, mit Ausnahme der benutzerdefinierten Nachrichtenklasse und des benutzerdefinierten Formulars, sollten Sie auch überlegen, wie Sie Konflikte zwischen Kopien eines Elements dieses Elementtyps Outlook behandeln möchten. Standardmäßig verwendet Outlook ein Lösungsschema, das allen Elementen gemeinsam ist, berücksichtigt keine Eigenschaften, die für einen Elementtyp spezifisch sind, und stellt widersprüchliche Kopien dar, damit der Benutzer eine Entscheidung treffen kann. Dies liegt daran, dass benutzerdefinierte Elementtypen möglicherweise benutzerdefinierte Felder im benutzerdefinierten Formular definieren und benutzerdefinierte Eigenschaften und benutzerdefinierten Code aufweisen können. Wenn Outlook elementspezifische Eigenschaften berücksichtigen und versuchen möchten, den Konflikt mit minimalem Benutzereingriff zu lösen, müssen Sie dies über eine Einstellung in der Windows Registrierung angeben. Dies kann auf zwei Arten erreicht werden: 
  
- Durch Anwenden einer Gruppenrichtlinieneinstellung auf den lokalen Computer, der den Registrierungsschlüssel ConflictMsgCls festlegt. Im folgenden Beispiel wird die Version "14.0" für Outlook 2010 angegeben: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Durch direktes Ändern des Benutzerregistrierungsschlüssels ConflictMsgCls. Im folgenden Beispiel wird die Version "14.0" für Outlook 2010 angegeben: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Das Festlegen der Konfliktlösung über eine Gruppenrichtlinie hat Vorrang vor der direkten Änderung des Benutzerregistrierungsschlüssels. Der Speicherort des Schlüssels in der Registrierung hängt von der Version von Outlook ab. Sie geben den Namen der benutzerdefinierten Nachrichtenklasse als Wert unter diesem Schlüssel an. Geben Sie den Typ des Werts als **DWORD** und die Daten des Werts als einen der Werte in der folgenden Tabelle an, je nach dem ausgewählten Auflösungsschema. 
  
|Daten  | Beschreibung  |
|:-----|:-----|
|0  <br/> |Allgemeine Elementauflösung, die eine Benutzerentscheidung erfordert, wie in Outlook 2002 und früheren Versionen verwendet.  <br/> |
|1  <br/> |Allgemeine Elementauflösung, die minimale Benutzereingriffe erfordert, wie in Outlook seit Outlook 2003 verwendet.  <br/> |
|2  <br/> |Für E-Mail-Elemente spezifische Auflösung.  <br/> |
|3  <br/> |Lösung speziell für Besprechungselemente.  <br/> |
|4   <br/> |Lösung speziell für Terminelemente.  <br/> |
|5  <br/> |Lösung speziell für Kontaktelemente.  <br/> |
|6   <br/> |Lösung speziell für Aufgabenelemente.  <br/> |
|7   <br/> |Auflösung, die für kurzlebige Notizelemente spezifisch ist.  <br/> |
|8   <br/> |Spezifisch für Journalelemente.  <br/> |
   
Wenn Sie eines der elementspezifischen Lösungsschemas (Schlüsseldaten 2 bis 8) angeben, versuchen Outlook, Konflikte in elementspezifischen Feldern (z. B. **Start-** und **Endfelder** eines Terminelements) automatisch ohne Benutzereingriff zu lösen. Wenn Outlook der Ansicht ist, dass die Lösung zu einem Verlust wesentlicher Daten führen kann, behält Outlook widersprüchliche Kopien im Ordner "Konflikte" bei, und Benutzer können zum Ordner "Konflikte" wechseln, um diese Elemente manuell neu aufzulösen und die automatische Lösung außer Kraft zu setzen. 
  
Verwenden Sie dasselbe Beispiel für Geschäftskontakte oben, wenn Sie das kontaktelementspezifische Auflösungsschema für die benutzerdefinierte Nachrichtenklasse IPM angeben **möchten. Contact.Business**, you can add it as a **DWORD** value under  `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls` , and specify 5 as the data. 
  
> [!NOTE]
> Outlook verwendet immer ein Lösungsschema, das für Terminelemente für benutzerdefinierte Nachrichtenklassen spezifisch ist, die auf der Terminnachrichtenklasse **IPM basieren. Termin** **(z. B. IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>Siehe auch

- [Outlook-Elementobjekte](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

