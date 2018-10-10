---
title: ConvertToString-Methode (RDS)
TOCTitle: ConvertToString Method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa1a4326cf318a9cbcddf8ebcdf584543ac8ebfb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475405"
---
# <a name="converttostring-method-rds"></a>ConvertToString-Methode (RDS)


**Betrifft**: Access 2013 | Office 2013 

Konvertiert ein [Recordset](recordset-object-ado.md)-Objekt in eine MIME-Zeichenfolge, die die Recordsetdaten darstellt.

## <a name="syntax"></a>Syntax

*DataFactory*. ConvertToString (*Recordset*)

## <a name="parameters"></a>Parameter

  - *DataFactory*

  - Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.

  - *Recordset*

  - Eine Objektvariable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Hinweise

Verwenden Sie bei ASP-Dateien **ConvertToString**, um das **Recordset** -Objekt in eine auf dem Server generierte HTML-Seite einzubetten, damit es auf den Clientcomputer transportiert wird.

**ConvertToString** lädt das **Recordset** -Objekt zunächst in die Tabellen des Cursordiensts und generiert anschließend einen Datenstrom im MIME-Format.

Mit Remote Data Service kann die MIME-Zeichenfolge auf dem Client erneut in ein voll funktionsfähiges **Recordset** -Objekt konvertiert werden. Er eignet sich hervorragend für die Behandlung von weniger als 400 Datenzeilen mit einer Breite von maximal 1024 Bytes pro Zeile. Sie sollten ihn jedoch nicht zur Übertragung von BLOB-Daten und umfangreichen Ergebnisgruppen über HTTP verwenden. Da die Zeichenfolge nicht komprimiert wird, kann die Übertragung von sehr großen Datensätzen über HTTP im Vergleich zum datenübertragungsoptimierten Tablegram-Format, das von Remote Data Service definiert und als dessen systemeigenes Transportprotokollformat verwendet wird, eine beträchtliche Zeit dauern.


> [!NOTE]
> <P>[!HINWEIS] Beachten Sie, dass die Größe der Zeichenfolge bei früheren Versionen von VBScript als Version 2.0 auf 32 KB beschränkt ist, wenn Sie Active Server Pages-Dateien verwenden, um die resultierende MIME-Zeichenfolge in den Client einer HTML-Seite einzubetten. Wenn diese Beschränkung überschritten wird, wird ein Fehler ausgegeben. Halten Sie den Abfrageumfang bei der MIME-Einbettung mithilfe von ASP-Dateien relativ gering. Laden Sie die aktuellste Version von VBScript von der <A href="https://www.microsoft.com/downloads/en/default.aspx">Microsoft Windows Script Technologies-Website</A> herunter, um dieses Problem zu beheben.</P>


