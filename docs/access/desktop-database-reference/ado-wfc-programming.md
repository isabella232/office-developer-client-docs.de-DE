---
title: ADO/WFC-Programmierung
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 63cfbdf2219179536bd4726d16e49fd05a84f4a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607549"
---
# <a name="adowfc-programming"></a>ADO/WFC-Programmierung

**Gilt für**: Access 2013, Office 2013

ADO wurde für Microsoft Visual J++ 6.0 so erweitert, dass auf folgende Weise die Zusammenarbeit mit Windows Foundation Classes (WFC) möglich ist. Erstens wurde ein Satz von Java-Klassen implementiert, durch den die ADO-Schnittstellen erweitert und für den Java-Programmierer interessante Benachrichtigungen erstellt werden. Außerdem machen die Java-Klassen Funktionen verfügbar, durch die Java-Typen an den Benutzer zurückgegeben werden. Zur Verbesserung der Leistung wird durch die Java-Klasse direkt auf die systemeigenen Datentypen im rowset-OLE DB-Objekt zugegriffen, die an den Java-Programmierer zurückgegeben werden, ohne erst in eine bzw. aus einer Variante konvertiert zu werden. ADO wurde außerdem erweitert, um mit Ereignisbenachrichtigungen im WFC-Framework zusammenzuarbeiten.

ADO für Windows Foundation Classes (ADO/WFC) unterstützt alle ADO-Standardmethoden, -eigenschaften, -objekte und -ereignisse. Operationen, für die eine Variante als Parameter erforderlich ist und die in einer Sprache wie Microsoft Visual Basic hervorragende Leistung bieten, zeigen in einer Sprache wie Visual J++ eine geringere Leistung. Aus diesem Grund werden von ADO/WFC Accessorfunktionen für das [Field](field-object-ado.md)-Objekt bereitgestellt, für die systemeigene Java-Datentypen anstelle der Variantendatentypen verwendet werden können.

Ausführlichere Informationen in der ADO-Dokumentation zu den ADO/WFC-Paketen finden Sie unter [dem ADO/WFC-Syntaxindex](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index).

## <a name="referencing-the-library"></a>Verweisen auf die Bibliothek

Fügen Sie die folgende Zeile in den Code ein, um die ADO/WFC-Datenklassen in das Projekt zu importieren:

```java 
 
import com.ms.wfc.data.*; 
```

