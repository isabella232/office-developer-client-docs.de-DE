---
title: Konvertieren von Microsoft Access-Tabellen, -Formularen und -Berichten
TOCTitle: Convert Microsoft Access Tables, Forms, and Reports
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f3928f3f0378c32737bc4881779b113c5d03774
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476111"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Konvertieren von Microsoft Access-Tabellen, -Formularen und -Berichten

**Betrifft**: Access 2013 | Office 2013

Verschiedene in Microsoft Access 2002 enthaltene Änderungen können Auswirkungen auf das Verhalten der Anwendungen der Version 1.*x* oder 2.0 haben. Die folgenden Abschnitte bieten genauere Informationen zu diesen Änderungen.

## <a name="indexes-and-relationships"></a>Indizes und Beziehungen

Eine Microsoft Access-Tabelle kann bis zu 32 Indizes enthalten. Sehr komplexe Tabellen, die Bestandteil vieler Beziehungen sind, können u. U. die Indexeinschränkung überschreiten, sodass Sie nicht in der Lage sind, die Datenbank mit diesen Tabellen zu konvertieren. Das Microsoft Access-Datenbankmodul erstellt Indizes auf beiden Seiten von Beziehungen zwischen Tabellen. Wenn sich Ihre Datenbank nicht konvertieren lässt, löschen Sie einige Beziehungen, und versuchen Sie dann erneut, die Datenbank zu konvertieren.

## <a name="the-limittolist-property-of-combo-boxes"></a>Die LimitToList-Eigenschaft von Kombinationsfeldern

In Microsoft Access 2002 oder höher, akzeptiert Kombinationsfelder **Null** -Werte, wenn die **LimitToList** -Eigenschaft auf **True** (– 1) festgelegt ist, ob die Liste **Null** -Werte enthält oder nicht. In Version 2.0 akzeptiert ein Kombinationsfeld, dessen **LimitToList** -Eigenschaft auf **True** festgelegt ist, nur dann einen **Null** -Wert, wenn die Liste einen **Null** -Wert enthält. Wenn Sie die Eingabe eines **Null** -Werts in ein Kombinationsfeld nicht zulassen möchten, legen Sie die **Required** -Eigenschaft des betreffenden Tabellenfelds auf **Ja** fest.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Menüs und direkte Bearbeitung von OLE-Objekten

Um während der direkten Bearbeitung von OLE-Objekten eine erweiterte Funktionalität zur Verfügung zu stellen, wurden einige Menübefehle in ein Menü verschoben, das beim Aktivieren eines OLE-Servers nicht ersetzt wird.

Von diesen Änderungen sind nicht die Makros Ihrer konvertierten Anwendung betroffen, die mithilfe der AusführenMenübefehl-Aktion einen Menübefehl der Version 2.0 ausführen, wenn eine Komponente aktiviert ist. Die Befehle der Version 2.0 werden in die entsprechenden Befehle neuerer Microsoft Access-Versionen umgewandelt.

## <a name="referencing-a-control-on-a-read-only-form"></a>Verweisen auf ein Steuerelement eines schreibgeschützten Formulars

In Microsoft Access 2002 oder höher können Sie nicht mithilfe eines Ausdrucks auf den Wert eines Steuerelements eines schreibgeschützten Formulars verweisen, das an eine leere Datenquelle gebunden ist. In früheren Versionen gab der Ausdruck einen **Null** -Wert zurück. Bevor Sie auf ein Steuerelement eines schreibgeschützten Formulars verweisen, stellen Sie sicher, dass die Datenquelle des Formulars Datensätze enthält.

## <a name="date-fields-and-data-entry"></a>Datumsfelder und Dateneingabe

Wenn Sie in ein Feld vom Typ Datum/Uhrzeit auf einem Formular- oder Tabellen-Datenblatt 3.3 eingeben, wird in Microsoft Access 2002 oder höher automatisch das aktuelle Jahr hinzugefügt. Wenn Sie in das gleiche Feld jedoch 3.3. eingeben, zeigt Microsoft Access eine Fehlermeldung an. Lassen Sie das letzte Datumstrennzeichen weg, damit Microsoft Access das Datum in das richtige Format übertragen kann.

## <a name="buttons-created-with-the-command-button-wizard"></a>Mit dem Befehlsschaltflächen-Assistent erstellte Schaltflächen

Wenn Sie in den Versionen 2.0 oder 7.0 von Microsoft Access mithilfe des Befehlsschaltflächen-Assistenten Code erstellt haben, der eine andere Anwendung aufruft, löschen Sie diese Schaltfläche, und erstellen Sie sie mithilfe des Befehlsschaltflächen-Assistenten in Microsoft Access 2002 oder höher erneut.

## <a name="form-and-report-class-modules"></a>Die Klassenmodule für Formulare und Berichte

In früheren Versionen von Microsoft Access 2002 sind ** **Formular-** und** Objekten Klassenmodule zugeordnet, auch wenn kein Code hinter dem Objekt vorhanden ist. In Microsoft Access 2002 oder höher, können Sie die **HasModule** -Eigenschaft eines Formulars oder Berichts auf **False**festlegen. Wenn Sie die **HasModule** -Eigenschaft auf **False**festlegen, des Formulars oder Berichts dauert weniger Speicherplatz und wird schneller geladen, da es nicht mehr mit einer zugeordneten Klassenmodul ist.

## <a name="converted-version-20-report-has-different-margins"></a>Konvertierter Version 2.0-Bericht besitzt andere Randeinstellungen

Probleme können auftreten, wenn Sie einen Bericht in Microsoft Access 2002 oder höher, der von Microsoft Access 2.0 konvertiert wurde und bei dem einige Ränder auf 0 festgelegt sind, drucken oder in der Seitenansicht anzeigen möchten. Wenn Sie einen Microsoft Access 2.0-Bericht konvertieren, werden die Ränder nicht auf 0 festgelegt, sondern auf den kleinsten Rand, der für den Standarddrucker zulässig ist. Dadurch können keine Berichtsdaten im nicht bedruckbaren Bereich des Druckers gedruckt werden.

Um das Problem zu beheben, verringern Sie die Spaltenbreite, den Spaltenabstand und/oder die Anzahl von Spalten im Bericht so, dass die Summe aus allen Spaltenbreiten und der Breite der Standardränder kleiner oder gleich der Papierbreite ist.

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Format-Eigenschaft kann nicht verwendet werden, um zwischen Null-Werten und leeren Zeichenfolgen zu unterscheiden.

In Versionen 1. *X* und 2.0 können die **Format** -Eigenschaft eines Steuerelements an unterschiedliche Werte für **Null** -Werte und leere Zeichenfolgen (""). In Microsoft Access 2002 oder höher, zur Unterscheidung zwischen **Null** -Werte und leere Zeichenfolgen in einem Steuerelement in einem Formular festgelegt **ControlSource** -Eigenschaft des Steuerelements an ein Ausdruck, der auf den Wert **Null** getestet. Legen Sie beispielsweise um "Null" oder "LZ" in einem Steuerelement anzuzeigen, die **ControlSource** -Eigenschaft auf den folgenden Ausdruck:

\=IIf (IsNull (\[MeinSteuerelement\]), "Null", Format (\[MeinSteuerelement\], "@; ;LZ"))"))

