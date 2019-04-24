---
title: Konvertieren von Microsoft Access-Tabellen,-Formularen und-Berichten
TOCTitle: Convert Microsoft Access tables, forms, and reports
description: Von Microsoft Access 2002 vorgenommene Änderungen können sich auf das Verhalten Ihrer Version 1. x-oder 2,0-Anwendungen auswirken.
ms:assetid: cc170e62-a663-60e8-4446-07a7a874b747
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834413(v=office.15)
ms:contentKeyID: 48547731
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5187104
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9c1ff7584269ce073a805edf8710bb3ea4eb1a36
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295583"
---
# <a name="convert-microsoft-access-tables-forms-and-reports"></a>Konvertieren von Microsoft Access-Tabellen,-Formularen und-Berichten

**Gilt für**: Access 2013, Office 2013

Verschiedene in Microsoft Access 2002 enthaltene Änderungen können Auswirkungen auf das Verhalten der Anwendungen der Version 1.*x* oder 2.0 haben. Die folgenden Abschnitte bieten genauere Informationen zu diesen Änderungen.

## <a name="indexes-and-relationships"></a>Indizes und Beziehungen

Eine Microsoft Access-Tabelle kann bis zu 32 Indizes enthalten. Sehr komplexe Tabellen, die Bestandteil vieler Beziehungen sind, können u. U. die Indexeinschränkung überschreiten, sodass Sie nicht in der Lage sind, die Datenbank mit diesen Tabellen zu konvertieren. Das Microsoft Access-Datenbankmodul erstellt Indizes auf beiden Seiten von Beziehungen zwischen Tabellen. Wenn sich Ihre Datenbank nicht konvertieren lässt, löschen Sie einige Beziehungen, und versuchen Sie dann erneut, die Datenbank zu konvertieren.

## <a name="the-limittolist-property-of-combo-boxes"></a>Die LimitToList-Eigenschaft der Kombinationsfelder

In Microsoft Access 2002 oder höher akzeptieren Kombinationsfelder **null** -Werte, wenn die **LimitToList** -Eigenschaft auf **true** (– 1) festgelegt ist, unabhängig davon, ob die Liste **null** -Werte enthält oder nicht. In Version 2.0 akzeptiert ein Kombinationsfeld, dessen **LimitToList** -Eigenschaft auf **True** festgelegt ist, nur dann einen **Null** -Wert, wenn die Liste einen **Null** -Wert enthält. Wenn Sie die Eingabe eines **Null** -Werts in ein Kombinationsfeld nicht zulassen möchten, legen Sie die **Required** -Eigenschaft des betreffenden Tabellenfelds auf **Ja** fest.

## <a name="menus-and-in-place-activation-of-ole-objects"></a>Menüs und direkte Aktivierung von OLE-Objekten

Um Ihnen während der Aktivierung von OLE-Objekten zusätzliche Funktionen zur Verfügung zu stellen, wurden möglicherweise einige Menübefehle in ein Menü verschoben, das beim Aktivieren eines OLE-Servers nicht ersetzt wird.

Macros in your converted application that use a DoMenuItem action to carry out a version 2.0 menu command when a component is activated won't be affected by the changes. Version 2.0 commands are mapped to their equivalents in later versions of Microsoft Access.

## <a name="referencing-a-control-on-a-read-only-form"></a>Verweisen auf ein Steuerelement auf einem schreibgeschützten Formular

In Microsoft Access 2002 oder höher können Sie nicht mithilfe eines Ausdrucks auf den Wert eines Steuerelements eines schreibgeschützten Formulars verweisen, das an eine leere Datenquelle gebunden ist. In früheren Versionen gab der Ausdruck einen **Null** -Wert zurück. Bevor Sie auf ein Steuerelement eines schreibgeschützten Formulars verweisen, stellen Sie sicher, dass die Datenquelle des Formulars Datensätze enthält.

## <a name="date-fields-and-data-entry"></a>Datumsfelder und Dateneingabe

If you enter **3/3** in a field of type Date on a form or a table datasheet, the current year is automatically added in Microsoft Access 2002 or later. However, if you enter **3/3/** in the same field, Microsoft Access returns an error message. You must omit the last date delimiter so that Microsoft Access can translate the date into the proper format.

## <a name="buttons-created-with-the-command-button-wizard"></a>Mit dem Befehlsschaltflächen-Assistenten erstellte Schaltflächen

Wenn Sie in den Versionen 2.0 oder 7.0 von Microsoft Access mithilfe des Befehlsschaltflächen-Assistenten Code erstellt haben, der eine andere Anwendung aufruft, löschen Sie diese Schaltfläche, und erstellen Sie sie mithilfe des Befehlsschaltflächen-Assistenten in Microsoft Access 2002 oder höher erneut.

## <a name="form-and-report-class-modules"></a>Formular-und Berichtsklassen Module

In versions of Microsoft Access prior to 2002, **Form** and **Report** objects have associated class modules even if there's no code behind the object. In Microsoft Access 2002 or later, you can set a form's or report's **HasModule** property to **False**. When you set the **HasModule** property to **False**, the form or report will take up less disk space and will load faster because it will no longer have an associated class module.

## <a name="converted-version-20-report-has-different-margins"></a>Konvertierter Version 2,0-Bericht hat unterschiedliche Ränder

Probleme können auftreten, wenn Sie einen Bericht in Microsoft Access 2002 oder höher, der von Microsoft Access 2.0 konvertiert wurde und bei dem einige Ränder auf 0 festgelegt sind, drucken oder in der Seitenansicht anzeigen möchten. Wenn Sie einen Microsoft Access 2.0-Bericht konvertieren, werden die Ränder nicht auf 0 festgelegt, sondern auf den kleinsten Rand, der für den Standarddrucker zulässig ist. Dadurch können keine Berichtsdaten im nicht bedruckbaren Bereich des Druckers gedruckt werden.

Um das Problem zu beheben, verringern Sie die Spaltenbreite, den Spaltenabstand und/oder die Anzahl von Spalten im Bericht so, dass die Summe aus allen Spaltenbreiten und der Breite der Standardränder kleiner oder gleich der Papierbreite ist.

## <a name="cant-use-the-format-property-to-distinguish-null-values-and-zero-length-strings"></a>Die Format-Eigenschaft kann nicht verwendet werden, um NULL-Werte und leere Zeichenfolgen zu unterscheiden.

In den Versionen 1. *x* und 2,0 können Sie die **Format** -Eigenschaft eines Steuerelements verwenden, um unterschiedliche Werte für **null** -Werte und leere Zeichenfolgen ("") anzuzeigen. In Microsoft Access 2002 or later, to distinguish between **Null** values and zero-length strings in a control on a form, set the control's **ControlSource** property to an expression that tests for the **Null** value case. For example, to display "Null" or "ZLS" in a control, set its **ControlSource** property to the following expression:

`=IIf(IsNull([MyControl]), "Null", Format([MyControl], "@;ZLS"))`

