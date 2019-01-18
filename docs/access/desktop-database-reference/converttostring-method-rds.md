---
title: ConvertToString-Methode (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2c589339eb838f944ce4443c19a787eafb01c3dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717727"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="8782c-102">ConvertToString-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="8782c-102">ConvertToString method (RDS)</span></span>

<span data-ttu-id="8782c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8782c-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="8782c-104">Konvertiert ein [Recordset](recordset-object-ado.md)-Objekt in eine MIME-Zeichenfolge, die die Recordsetdaten darstellt.</span><span class="sxs-lookup"><span data-stu-id="8782c-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8782c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8782c-105">Syntax</span></span>

<span data-ttu-id="8782c-106">*DataFactory*. ConvertToString (*Recordset*)</span><span class="sxs-lookup"><span data-stu-id="8782c-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="8782c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8782c-107">Parameters</span></span>

|<span data-ttu-id="8782c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8782c-108">Parameter</span></span>|<span data-ttu-id="8782c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8782c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8782c-110">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="8782c-110">*DataFactory*</span></span> |<span data-ttu-id="8782c-111">Eine Objektvariable, die ein [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8782c-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="8782c-112">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="8782c-112">*Recordset*</span></span> |<span data-ttu-id="8782c-113">Eine Objektvariable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8782c-113">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8782c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8782c-114">Remarks</span></span>

<span data-ttu-id="8782c-115">Verwenden Sie bei ASP-Dateien **ConvertToString**, um das **Recordset** -Objekt in eine auf dem Server generierte HTML-Seite einzubetten, damit es auf den Clientcomputer transportiert wird.</span><span class="sxs-lookup"><span data-stu-id="8782c-115">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="8782c-116">**ConvertToString** lädt das **Recordset** -Objekt zunächst in die Tabellen des Cursordiensts und generiert anschließend einen Datenstrom im MIME-Format.</span><span class="sxs-lookup"><span data-stu-id="8782c-116">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="8782c-p101">Mit Remote Data Service kann die MIME-Zeichenfolge auf dem Client erneut in ein voll funktionsfähiges **Recordset** -Objekt konvertiert werden. Er eignet sich hervorragend für die Behandlung von weniger als 400 Datenzeilen mit einer Breite von maximal 1024 Bytes pro Zeile. Sie sollten ihn jedoch nicht zur Übertragung von BLOB-Daten und umfangreichen Ergebnisgruppen über HTTP verwenden. Da die Zeichenfolge nicht komprimiert wird, kann die Übertragung von sehr großen Datensätzen über HTTP im Vergleich zum datenübertragungsoptimierten Tablegram-Format, das von Remote Data Service definiert und als dessen systemeigenes Transportprotokollformat verwendet wird, eine beträchtliche Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="8782c-p101">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**. It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row. You shouldn't use it for streaming BLOB data and large result sets over HTTP. No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>

> [!NOTE]
> <span data-ttu-id="8782c-p102">[!HINWEIS] Beachten Sie, dass die Größe der Zeichenfolge bei früheren Versionen von VBScript als Version 2.0 auf 32 KB beschränkt ist, wenn Sie Active Server Pages-Dateien verwenden, um die resultierende MIME-Zeichenfolge in den Client einer HTML-Seite einzubetten. Wenn diese Beschränkung überschritten wird, wird ein Fehler ausgegeben. Halten Sie den Abfrageumfang bei der MIME-Einbettung mithilfe von ASP-Dateien relativ gering. Laden Sie die aktuellste Version von VBScript von der [Microsoft Windows Script Technologies-Website](https://www.microsoft.com/download/default.aspx) herunter, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="8782c-p102">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K. If this limit is exceeded, an error is returned. Keep the query scope relatively small when using MIME embedding via .asp files. To fix this, download the latest version of VBScript from the [Microsoft Download Center](https://www.microsoft.com/download/default.aspx).</span></span>


