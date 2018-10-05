---
title: Informationen zur Konfliktbehebung für benutzerdefinierte Typen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: In diesem Thema wird beschrieben, wie zum Lösen von Konflikten für benutzerdefinierte Elementtypen, die Sie in Outlook erstellen.
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382988"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Informationen zur Konfliktbehebung für benutzerdefinierte Typen

In diesem Thema wird beschrieben, wie zum Lösen von Konflikten für benutzerdefinierte Elementtypen, die Sie in Outlook erstellen.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Konfliktbehebung für standard-Outlook-Elementtypen

In Outlook Konflikte auftreten, wenn zwei oder mehr Kopien desselben Elements unabhängig voneinander geändert wurden. Outlook erkennt Konflikte, während der Synchronisierung. Beispielsweise können Sie ein Besprechungselement online in Outlook Web App aktualisieren und dann dasselbe Besprechungselement in Outlook aktualisieren, wenn Sie offline arbeiten. Wenn Outlook wieder online geht und die Daten zwischen dem Client und dem Server synchronisiert, erkennt er, dass zwei unterschiedliche Kopien von der gleichen Besprechungselement vorhanden sind.
  
Wenn Outlook Elemente synchronisiert, die eine standard-Outlook-Elementtyp angehören, wird es berücksichtigt die Eigenschaften, die spezifisch für diesen Artikel zum Erkennen von Konflikten möglicher sind. Outlook versucht, das Lösen von Konflikten und speichert die resultierende Kopie in den entsprechenden Ordner ohne Benutzereingriff anzufordern. In Fällen, wenn Outlook der Auffassung, dass es besteht die Möglichkeit, dass die resultierende Kopie möglicherweise nicht alle wichtige Daten enthält, speichert Outlook die miteinander in Konflikt stehende Kopien im Ordner Konflikte unterhalb des Ordners Synchronisierungsprobleme. 
  
> [!NOTE]
> Synchronisierungsprobleme und den zugehörigen Unterordnern sind ausgeblendet, bis Sie **Ordnerliste** im Navigationsbereich klicken. 
  
In solchen Fällen können Benutzer wechseln zu dem Ordner Konflikte, um zu überprüfen, welche Elemente in Konflikt wurden und ob eine Kopie im Ordner Konflikte verwenden, um die Kopie zu ersetzen, bei der Outlook entschieden, die beibehalten werden.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Konfliktbehebung für benutzerdefinierte Elementtypen

### <a name="item-types-and-message-classes"></a>Elementtypen und Nachrichtenklassen
  
Alle Elemente in Outlook sind eine Nachrichtenklasse zugeordnet. In der Standardeinstellung ist beispielsweise ein e-Mail-Element zugeordnet, mit der Nachrichtenklasse IPM **. Hinweis**. Die Nachrichtenklasse wird hauptsächlich verwendet, um das Formular zu identifizieren, das zum Anzeigen des Elements in Outlook verwendet werden soll. Outlook unterstützt eine Liste der Nachrichtenklassen, die die Typen von Elementen in Outlook integriert zugeordnet sind. Weitere Informationen zu Nachrichtenklassen finden Sie unter [Elementtypen und Meldungsklassen](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Benutzer können benutzerdefinierte Elementtypen erstellen, weisen Sie die benutzerdefinierten Elementtypen benutzerdefinierte Nachrichtenklassen und lassen Sie Outlook, die ein benutzerdefiniertes Formular verwenden, um die benutzerdefinierten Elementtypen anzuzeigen. Beispielsweise sollten Sie Outlook zum Anzeigen eines benutzerdefinierten Kontaktformulars für Kontakten. Dazu können Sie eine benutzerdefinierte Nachrichtenklasse IPM **erstellen. Contact.Business**, erstellen Sie ein benutzerdefiniertes Formular für diese Nachrichtenklasse und Geschäftskontakten mit dieser Nachrichtenklasse zuweisen. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registrieren einen Konflikt Lösungsschema für benutzerdefinierte Elementtypen
  
Wenn Sie einen benutzerdefinierten Elementtyp, außer die benutzerdefinierte Nachrichtenklasse und ein benutzerdefiniertes Formular erstellen sollten Sie außerdem, wie Outlook so verarbeiten Sie Konflikte zwischen den Kopien eines Elements der diesen Elementtyp. Outlook standardmäßig ein, die alle Elemente Lösungsschema beschäftigt, berücksichtigt keine Eigenschaften, die speziell für ein Elementtyp und miteinander in Konflikt stehende Kopien für den Benutzer zum Treffen einer Entscheidung präsentiert. Dies ist, da benutzerdefinierte Elementtypen können benutzerdefinierte Felder in der benutzerdefinierten Formular definieren, und weist möglicherweise benutzerdefinierte Eigenschaften und benutzerdefinierter Code. Wenn Sie möchten, dass Outlook berücksichtigt elementspezifische Eigenschaften, und versuchen, den Konflikt mit minimalem Benutzereingriff zu beheben, müssen Sie, die durch eine Einstellung in der Windows-Registrierung angeben. Dies kann auf zwei Arten erreicht werden: 
  
- Durch Anwenden einer gruppenrichtlinieneinstellung auf dem lokalen Computer festgelegt wird, der den Registrierungsschlüssel ConflictMsgCls. Das folgende Beispiel gibt die Version "14.0" für Outlook 2010: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Den Benutzer Registrierungsschlüssel ConflictMsgCls direkt geändert. Das folgende Beispiel gibt die Version "14.0" für Outlook 2010: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Festlegen der Konfliktbehebung mithilfe von Gruppenrichtlinien hat Vorrang vor den Registrierungsschlüssel Benutzer direkt zu ändern. Der Speicherort des Schlüssels in der Registrierung, hängt von der Version von Outlook. Sie geben den Namen der benutzerdefinierten Nachrichtenklasse als Wert unter diesem Schlüssel. Geben Sie den Typ des Werts als **DWORD-Wert**und die Daten des Werts als einen der Werte in der folgenden Tabelle, abhängig von der gewählten Lösungsschema dargestellt. 
  
|Daten  | Beschreibung  |
|:-----|:-----|
|0  <br/> |Allgemeine Element-Lösung, die eine Entscheidung Benutzer erforderlich sind, wie in Outlook 2002 und früheren Versionen.  <br/> |
|1  <br/> |Allgemeine Element-Lösung, die möglichst wenig Eingreifen erfordert, wie in Outlook seit Outlook 2003 verwendet.  <br/> |
|2  <br/> |Auflösung von bestimmten e-Mail-Elemente.  <br/> |
|3  <br/> |Spezifische Lösung für Besprechungsanfragen.  <br/> |
|4  <br/> |Auflösung von speziell für Terminelemente.  <br/> |
|5  <br/> |Spezifische Lösung für Kontaktelemente.  <br/> |
|6  <br/> |Auflösung von speziell für Aufgabenelemente.  <br/> |
|7  <br/> |Auflösung von speziell für Kurznotiz Elemente.  <br/> |
|8  <br/> |Auflösung von speziell für Journalelemente.  <br/> |
   
Wenn Sie eines der Schemas elementspezifische Auflösung (Registrierungsschlüsseldaten 2 bis 8) angeben, versucht Outlook zum Lösen von Konflikten in elementspezifische Felder (beispielsweise **Start** und **End** Felder eines Besprechungselements automatisch und ohne Benutzereingriff) . Outlook hält, dass die Lösung in den Verlust von wichtigen Daten führen kann, Outlook miteinander in Konflikt stehende Kopien im Ordner Konflikte beibehalten wird, und Benutzer können auswählen, wechseln zum Ordner Konflikte manuell erneut aufgelöst dieser Elemente und überschreiben Sie den Einstellungsmodus automatisch Auflösung. 
  
Unter Verwendung derselben Business Kontakte obigen Beispiel, wenn Sie den Kontakt elementspezifische Lösungsschema für die benutzerdefinierte Nachrichtenklasse IPM **angeben möchten. Contact.Business**, können Sie es als einen **DWORD-** Wert unter Hinzufügen `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls`, und geben Sie 5 als Daten. 
  
> [!NOTE]
> Outlook verwendet immer eine Lösungsschema, die speziell für Terminelemente für benutzerdefinierte Nachrichtenklassen ist, die auf der Termin Nachrichtenklasse IPM **basieren. Termin** (beispielsweise **IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>Siehe auch

- [Outlook-Elementobjekte](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

