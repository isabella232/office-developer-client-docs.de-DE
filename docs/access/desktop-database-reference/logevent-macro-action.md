---
title: LogEvent-Makroaktion
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edc2fcaa72f6bfb912708948903aa09b25447580
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998173"
---
# <a name="logevent-macro-action"></a>LogEvent-Makroaktion

**Betrifft**: Access 2013, Office 2013

Mit der **ProtokollierenEreignis** -Aktion werden Informationen in die **USysApplicationLog** -Systemtabelle geschrieben.

> [!NOTE]
> [!HINWEIS] Die **ProtokollierenEreignis** -Aktion ist nur in Datenmakros verfügbar.

## <a name="setting"></a>Einstellung

Die **ProtokollierenEreignis** -Aktion kann mit den folgenden Argumenten verwendet werden.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Eingabe erforderlich</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Beschreibung</strong></p></td>
<td><p>Nein</p></td>
<td><p>Ein Zeichenfolgenausdruck, der die Bedingung beschreibt, die Sie protokollieren möchten. Die Länge der Beschreibung darf 255 Zeichen nicht überschreiten.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Hinweise

Mit der **ProtokollierenEreignis** -Aktion können Sie in der **USysApplicationLog** -Systemtabelle Statusinformationen schreiben, für die nicht mit der **[AuslösenFehler](raiseerror-macro-action.md)** -Aktion ein Fehler ausgelöst werden muss. Beispielsweise können Sie Änderungen in einem bestimmten Feld protokollieren oder die Einträge in **USysApplicationLog** beim Debuggen des Makros verwenden.

Wenn Sie die **ProtokollierenEreignis** -Aktion zum Schreiben in der **USysApplicationLog** -Tabelle verwenden, wird die **Kategorie** -Spalte automatisch auf **Benutzer** festgelegt.

Zum Anzeigen der **USysApplicationLog** -Tabelle gehen Sie wie folgt vor:

1.  Klicken Sie im Menü **Datei** auf **Optionen**.

2.  Klicken Sie im Dialogfeld **Access-Optionen** auf die Registerkarte **Aktuelle Datenbank**.

3.  Klicken Sie im Bereich **Navigation** auf **Navigationsoptionen**.

4.  Klicken Sie im Dialogfeld **Navigationsoptionen** auf **Systemobjekte anzeigen** und dann auf **OK**.

5.  Klicken Sie auf **OK**, um das Dialogfeld **Access-Optionen** zu schließen.

