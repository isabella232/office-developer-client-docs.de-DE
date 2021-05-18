---
title: Informationen zur Konfliktbehebung für benutzerdefinierte Typen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: In diesem Thema wird beschrieben, wie Sie Konflikte für benutzerdefinierte Elementtypen lösen, die Sie in Outlook.
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316947"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Informationen zur Konfliktbehebung für benutzerdefinierte Typen

In diesem Thema wird beschrieben, wie Sie Konflikte für benutzerdefinierte Elementtypen lösen, die Sie in Outlook.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Konfliktauflösung für Standardelementtypen Outlook Elementtypen

In Outlook Konflikte auftreten, wenn zwei oder mehr Kopien desselben Elements unabhängig voneinander geändert wurden. Outlook erkennt Konflikte während der Synchronisierung. Beispielsweise können Sie ein Besprechungselement online in Outlook Web App aktualisieren und dann dasselbe Besprechungselement in Outlook offline arbeiten. Wenn Outlook erneut online geht und die Daten zwischen dem Clientcomputer und dem Server synchronisiert, wird erkannt, dass es zwei verschiedene Kopien desselben Besprechungselements gibt.
  
Wenn Outlook Elemente synchronisiert, die zu einem Standardelementtyp Outlook gehören, werden die eigenschaften berücksichtigt, die für diesen Elementtyp spezifisch sind, um mögliche Konflikte zu erkennen. Outlook versucht, Konflikte zu lösen, und speichert die sich aus dem Ordner resultierende Kopie ohne Benutzereingriff. In Fällen, in denen Outlook der Ansicht ist, dass die ergebnisende Kopie möglicherweise nicht alle wichtigen Daten enthält, speichert Outlook die in Konflikt enden Kopien im Ordner Konflikte unter dem Ordner Synchronisierungsprobleme. 
  
> [!NOTE]
> Synchronisierungsprobleme und ihre Unterordner werden ausgeblendet, bis Sie im Navigationsbereich **auf** Ordnerliste klicken. 
  
In solchen Fällen können Benutzer zum Ordner Konflikte wechseln, um zu überprüfen, welche Elemente in Konflikt waren und ob eine Kopie im Ordner Konflikte verwendet werden soll, um die Kopie zu ersetzen, die Outlook beibehalten hat.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Konfliktauflösung für benutzerdefinierte Elementtypen

### <a name="item-types-and-message-classes"></a>Elementtypen und Meldungsklassen
  
Alle Elemente in Outlook einer Nachrichtenklasse zugeordnet. Beispielsweise ist der Nachrichtenklasse IPM standardmäßig ein E-Mail-Element **zugeordnet. Hinweis**. Die Nachrichtenklasse wird in erster Linie verwendet, um das Formular zu identifizieren, das zum Anzeigen des Elements in der Outlook. Outlook unterstützt eine Liste von Nachrichtenklassen, die den Typen von Elementen zugeordnet sind, die in die Outlook. Weitere Informationen zu Nachrichtenklassen finden Sie unter [Elementtypen und Meldungsklassen](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Benutzer können benutzerdefinierte Elementtypen erstellen, benutzerdefinierte Nachrichtenklassen benutzerdefinierten Elementtypen zuweisen und Outlook benutzerdefinierten Elementtypen mithilfe eines benutzerdefinierten Formulars anzeigen. Sie können z. B. Outlook ein benutzerdefiniertes Geschäftskontaktformular für Ihre Geschäftskontakte anzeigen. Dazu können Sie eine benutzerdefinierte Nachrichtenklasse **IPM erstellen. Contact.Business**, erstellen Sie ein benutzerdefiniertes Formular für diese Nachrichtenklasse, und weisen Sie dieser Nachrichtenklasse Geschäftskontakte zu. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registrieren eines Konfliktlösungsschemas für benutzerdefinierte Elementtypen
  
Wenn Sie einen benutzerdefinierten Elementtyp erstellen, der nicht die benutzerdefinierte Nachrichtenklasse und das benutzerdefinierte Formular ist, sollten Sie auch überlegen, wie Sie Outlook konflikte zwischen Kopien eines Elements dieses Elementtyps behandeln möchten. Standardmäßig verwendet Outlook ein lösungsschema, das allen Elementen gemeinsam ist, keine Eigenschaften, die für einen Elementtyp spezifisch sind, und stellt widersprüchliche Kopien für den Benutzer zur Entscheidung vor. Dies liegt daran, dass benutzerdefinierte Elementtypen benutzerdefinierte Felder im benutzerdefinierten Formular definieren können und über benutzerdefinierte Eigenschaften und benutzerdefinierten Code verfügen. Wenn Sie Outlook elementspezifische Eigenschaften berücksichtigen und versuchen möchten, den Konflikt mit minimalem Benutzereingriff zu lösen, müssen Sie dies über eine Einstellung in der registrierungsspezifischen Windows angeben. Dies kann auf zwei Arten erreicht werden: 
  
- Durch Anwenden einer Gruppenrichtlinieneinstellung auf den lokalen Computer, der den Registrierungsschlüssel ConflictMsgCls festlegen. Im folgenden Beispiel wird die Version "14.0" für Outlook 2010 angegeben: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Durch direktes Ändern des Benutzerregistrierungsschlüssels ConflictMsgCls. Im folgenden Beispiel wird die Version "14.0" für Outlook 2010 angegeben: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Das Festlegen der Konfliktlösung über Gruppenrichtlinien hat Vorrang vor dem direkten Ändern des Benutzerregistrierungsschlüssels. Der Speicherort des Schlüssels in der Registrierung hängt von der Version des Outlook. Sie geben den Namen der benutzerdefinierten Nachrichtenklasse als Wert unter diesem Schlüssel an. Geben Sie den Typ des Werts als **DWORD** und die Daten des Werts als einen der Werte in der folgenden Tabelle an, je nach dem von Ihnen verwendeten Auflösungsschema. 
  
|Daten  | Beschreibung  |
|:-----|:-----|
|0  <br/> |Allgemeine Elementauflösung, die eine Benutzerentscheidung erfordert, wie in Outlook 2002 und früheren Versionen verwendet.  <br/> |
|1  <br/> |Allgemeine Elementauflösung, die minimale Benutzereingriffe erfordert, wie in Outlook seit Outlook 2003 verwendet.  <br/> |
|2  <br/> |Lösung speziell für E-Mail-Elemente.  <br/> |
|3  <br/> |Lösung speziell für Besprechungselemente.  <br/> |
|4   <br/> |Lösung speziell für Terminelemente.  <br/> |
|5   <br/> |Lösung, die für Kontaktelemente spezifisch ist.  <br/> |
|6   <br/> |Lösung, die für Vorgangselemente spezifisch ist.  <br/> |
|7   <br/> |Auflösung, die speziell für scheinige Notizenelemente spezifisch ist.  <br/> |
|8   <br/> |Lösung, die für Journalelemente spezifisch ist.  <br/> |
   
Wenn Sie eines der elementspezifischen Lösungsschemas (Schlüsseldaten 2 bis 8) angeben, versucht Outlook, Konflikte in elementspezifischen Feldern (z. B. **Start-** und **Endfelder** eines Terminelements) automatisch ohne Benutzereingriff zu lösen. Wenn Outlook der Meinung ist, dass die Lösung zum Verlust wichtiger Daten führen kann, behält Outlook im Ordner Konflikte widersprüchliche Kopien bei, und Benutzer können zum Ordner Konflikte wechseln, um diese Elemente manuell neu zu lösen und die automatische Lösung außer Kraft zu setzen. 
  
Verwenden Sie das oben beschriebene Beispiel für Geschäftskontakte, wenn Sie das kontaktelementspezifische Lösungsschema für die benutzerdefinierte Nachrichtenklasse **IPM angeben möchten. Contact.Business** können Sie ihn als **DWORD-Wert** unter hinzufügen und  `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls` 5 als Daten angeben. 
  
> [!NOTE]
> Outlook verwendet immer ein Lösungsschema, das für Terminelemente für benutzerdefinierte Nachrichtenklassen spezifisch ist, die auf der Terminnachrichtenklasse **IPM basieren. Appointment** (z. **B. IPM. Appointment.Personal**). 
  
## <a name="see-also"></a>Siehe auch

- [Outlook-Elementobjekte](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

