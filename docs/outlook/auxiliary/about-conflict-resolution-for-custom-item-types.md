---
title: Informationen zur Konfliktbehebung für benutzerdefinierte Typen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: In diesem Thema wird beschrieben, wie Konflikte für benutzerdefinierte Elementtypen, die Sie in Outlook erstellen, aufgelöst werden.
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316947"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>Informationen zur Konfliktbehebung für benutzerdefinierte Typen

In diesem Thema wird beschrieben, wie Konflikte für benutzerdefinierte Elementtypen, die Sie in Outlook erstellen, aufgelöst werden.
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>Konfliktbehebung für standardmäßige Outlook-Elementtypen

In Outlook treten Konflikte auf, wenn mindestens zwei Kopien desselben Elements unabhängig voneinander geändert wurden. Outlook erkennt Konflikte während der Synchronisierung. Sie können beispielsweise ein Besprechungselement Online in Outlook Web App aktualisieren und dann dasselbe Besprechungselement in Outlook aktualisieren, wenn Sie offline arbeiten. Wenn Outlook wieder online geht und die Daten zwischen dem Clientcomputer und dem Server synchronisiert, erkennt es, dass es zwei verschiedene Kopien desselben Besprechungselements gibt.
  
Wenn Outlook Elemente synchronisiert, die zu einem standardmäßigen Outlook-Elementtyp gehören, berücksichtigt es die Eigenschaften, die für diesen Elementtyp spezifisch sind, um mögliche Konflikte zu identifizieren. Outlook versucht, Konflikte aufzulösen und die resultierende Kopie im entsprechenden Ordner zu speichern, ohne Benutzereingriff anzufordern. In Fällen, in denen Outlook der Ansicht ist, dass die resultierende Kopie nicht alle wesentlichen Daten enthalten kann, speichert Outlook die in Konflikt stehenden Kopien im Ordner "Konflikte" unter dem Ordner "SynchronisierungsProbleme". 
  
> [!NOTE]
> SynchronisierungsProbleme und die zugehörigen Unterordner werden ausgeblendet, bis Sie im Navigationsbereich auf **Ordnerliste** klicken. 
  
In solchen Fällen können Benutzer sich für den Ordner Konflikte entscheiden, um zu überprüfen, welche Elemente in Konflikt stehen und ob eine Kopie im Ordner "Konflikte" verwendet werden soll, um die Kopie zu ersetzen, die Outlook beizubehalten hat.
  
## <a name="conflict-resolution-for-custom-item-types"></a>Konfliktbehebung für benutzerdefinierte Elementtypen

### <a name="item-types-and-message-classes"></a>Elementtypen und Meldungsklassen
  
Alle Elemente in Outlook sind einer Nachrichtenklasse zugeordnet. Standardmäßig ist ein e-Mail-Element beispielsweise der Nachrichtenklasse **IPM zugeordnet. Hinweis**. Die Message-Klasse wird hauptsächlich verwendet, um das Formular zu identifizieren, das zum Anzeigen des Elements in Outlook verwendet werden soll. Outlook unterstützt eine Liste der Nachrichtenklassen, die den in Outlook integrierten Elementtypen zugeordnet sind. Weitere Informationen zu Nachrichtenklassen finden Sie unter [Elementtypen und Meldungsklassen](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx). 
  
Benutzer können benutzerdefinierte Elementtypen erstellen, den benutzerdefinierten Elementtypen Benutzerdefinierte Nachrichtenklassen zuweisen und in Outlook ein benutzerdefiniertes Formular zum Anzeigen der benutzerdefinierten Elementtypen verwenden. Es kann beispielsweise sein, dass Outlook ein benutzerdefiniertes Geschäftskontaktformular für Ihre Geschäftskontakte anzeigen soll. Zu diesem Zweck können Sie eine benutzerdefinierte Nachrichtenklasse **IPM erstellen. Contact. Business**, erstellen Sie ein benutzerdefiniertes Formular für diese Nachrichtenklasse, und weisen Sie Geschäftskontakte dieser Nachrichtenklasse zu. 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>Registrieren eines Konfliktlösungsschemas für benutzerdefinierte Elementtypen
  
Wenn Sie einen benutzerdefinierten Elementtyp außer der benutzerdefinierten Nachrichtenklasse und benutzerdefiniertes Formular erstellen, sollten Sie auch überlegen, wie Outlook Konflikte zwischen Kopien eines Elements dieses Elementtyps behandeln soll. Standardmäßig verwendet Outlook ein Auflösungs Schema, das für alle Elemente gilt, keine Eigenschaften, die für einen Elementtyp spezifisch sind, und in Konflikt stehende Kopien für den Benutzer, um eine Entscheidung zu treffen. Der Grund ist, dass benutzerdefinierte Elementtypen Benutzerdefinierte Felder im benutzerdefinierten Formular definieren können und benutzerdefinierte Eigenschaften und benutzerdefinierten Code aufweisen können. Wenn Sie möchten, dass Outlook Element spezifische Eigenschaften berücksichtigt, und versuchen, den Konflikt mit minimalem Benutzereingriff zu beheben, müssen Sie dies über eine Einstellung in der Windows-Registrierung angeben. Dies kann auf zweierlei Weise erreicht werden: 
  
- Durch Anwenden einer Gruppenrichtlinieneinstellung auf den lokalen Computer, der den Registrierungsschlüssel ConflictMsgCls festlegt. Das folgende Beispiel gibt die Version "14,0" für Outlook 2010 an: 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- Durch direktes Ändern des Benutzer Registrierungsschlüssels ConflictMsgCls. Das folgende Beispiel gibt die Version "14,0" für Outlook 2010 an: 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
Das Festlegen der Konfliktbehebung über Gruppenrichtlinien hat Vorrang vor dem direkten Ändern des Benutzer Registrierungsschlüssels. Der Speicherort des Schlüssels in der Registrierung hängt von der Version von Outlook ab. Sie geben den Namen der benutzerdefinierten Nachrichtenklasse als Wert unter diesem Schlüssel an. Geben Sie je nach ausgewähltem Lösungsschema den Typ des Werts als **DWORD**-Wert und die Daten des Werts als einen der in der folgenden Tabelle aufgeführten Werte an. 
  
|Daten  | Beschreibung  |
|:-----|:-----|
|0  <br/> |Allgemeine Element Auflösung, die eine Benutzerentscheidung erfordert, wie in Outlook 2002 und früheren Versionen verwendet.  <br/> |
|1  <br/> |Allgemeine Element Auflösung, die nur minimale Benutzereingriffe erfordert, wie in Outlook seit Outlook 2003.  <br/> |
|2  <br/> |Auflösung speziell für e-Mail-Elemente.  <br/> |
|3  <br/> |Lösung, die für Besprechungselemente spezifisch ist.  <br/> |
|4  <br/> |Lösung, die für Termin Elemente spezifisch ist.  <br/> |
|5  <br/> |Lösung für Kontaktelemente.  <br/> |
|6  <br/> |Lösung, die für Aufgabenelemente spezifisch ist.  <br/> |
|7  <br/> |Eine Lösung, die für Kurznotiz-Elemente spezifisch ist.  <br/> |
|8  <br/> |Lösung, die für Journalelemente spezifisch ist.  <br/> |
   
Wenn Sie eines der elementspezifischen Auflösungs Schemas angeben (Schlüsseldaten 2 bis 8), versucht Outlook, Konflikte in elementspezifischen Feldern (beispielsweise **Start** -und Endfeld eines **** Terminelements) automatisch ohne Benutzereingriff aufzulösen. . Wenn Outlook der Ansicht ist, dass die Lösung zu einem Verlust wesentlicher Daten führen kann, werden in Outlook in Konflikt stehende Kopien im Ordner "Konflikte" gespeichert, und Benutzer können sich für den Ordner "Konflikte" entscheiden, um diese Elemente manuell erneut aufzulösen und die automatische Lösung. 
  
Verwenden Sie oben dasselbe Beispiel für Geschäftskontakte, wenn Sie das Kontaktelement spezifische Auflösungs Schema für die benutzerdefinierte Nachrichtenklasse **IPM angeben möchten. Contact. Business**, können Sie es als **DWORD** -Wert unter `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls`hinzufügen, und geben Sie 5 als Daten. 
  
> [!NOTE]
> Outlook verwendet immer ein Auflösungs Schema, das für Termin Elemente für benutzerdefinierte Nachrichtenklassen spezifisch ist, die auf der Termin Nachrichtenklasse, **IPM basieren. Termin** (beispielsweise **IPM. Termin. Personal**). 
  
## <a name="see-also"></a>Siehe auch

- [Outlook-Elementobjekte](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

