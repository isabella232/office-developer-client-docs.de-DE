---
title: Open-Methode (ADO-Recordset)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a753ea57fba54f2e3b1a08c93f1309259f712446
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947707"
---
# <a name="open-method-ado-recordset"></a>Open-Methode (ADO-Recordset)


**Betrifft**: Access 2013, Office 2013


Öffnet einen Cursor.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. Öffnen Sie*Source*, *ActiveConnection*, *CursorType*, *LockType*, *Optionen*

## <a name="parameters"></a>Parameter

  - *Source*

  - Optional. Ein **Variant** -Wert, der ausgewertet ein gültiges [Command](command-object-ado.md)-Objekt, eine SQL-Anweisung, einen Tabellennamen, den Aufruf einer gespeicherten Prozedur, eine URL oder den Namen einer Datei oder eines [Stream](stream-object-ado.md)-Objekts mit einem dauerhaft gespeicherten [Recordset](recordset-object-ado.md)-Objekt ergibt.

  - *ActiveConnection*

  - Optional. Ein **Variant** -Wert, der den Namen einer gültigen [Connection](connection-object-ado.md)-Objektvariablen ergibt, oder ein **String** -Wert, der [ConnectionString](connectionstring-property-ado.md)-Parameter enthält.

  - *CursorType*

  - Optional. Ein [CursorTypeEnum](cursortypeenum.md)-Wert, der den Cursortyp bestimmt, den der Anbieter zum Öffnen des **Recordset** -Objekts verwenden soll. Der Standardwert ist **adOpenForwardOnly**.

  - *LockType*

  - Optional. Ein [LockTypeEnum](locktypeenum.md)-Wert, der den Sperrtyp (vollständige Parallelität) bestimmt, den der Anbieter zum Öffnen des **Recordset** -Objekts verwenden sollte. Der Standardwert lautet **adLockReadOnly**.

  - *Options*

  - Optional. Ein **Long** -Wert, der angibt, wie der Anbieter das Argument *Source* auswerten soll, falls es etwas anderes als ein **Command** -Objekt darstellt, oder das **Recordset-Objekt** aus einer Datei, in der es vorher gespeichert wurde, wiederhergestellt werden soll. Es kann sich um einen oder mehrere [CommandTypeEnum](commandtypeenum.md)-Werte oder [ExecuteOptionEnum](executeoptionenum.md)-Werte handeln, die mit einem bitweisen AND-Operator kombiniert werden können.


> [!NOTE]
> <P>[!HINWEIS] Wenn Sie ein <STRONG>Recordset</STRONG> -Objekt aus einem <STRONG>Stream</STRONG> -Objekt, das ein permanentes <STRONG>Recordset</STRONG> -Objekt enthält, mithilfe eines <STRONG>ExecuteOptionEnum</STRONG> -Werts <STRONG>adAsyncFetchNonBlocking</STRONG> öffnen, hat dies keine Auswikungen. Der Abruf ist synchron und blockierend.</P>



Die **ExecuteOpenEnum** -Werte für **adExecuteNoRecords** oder **adExecuteStream** sollten nicht mit **Open** verwendet werden.

## <a name="remarks"></a>Hinweise

Bei dem Standardcursor für ein **Recordset** -Objekt in ADO handelt es sich um einen vorwärtsgerichteten, schreibgeschützten Cursor, der sich auf dem Server befindet.

Mithilfe der **Open** -Methode für ein **Recordset** -Objekt können Sie einen Cursor öffnen, der Datensätze aus einer Basistabelle, die Ergebnisse einer Abfrage oder ein zuvor gespeichertes **Recordset** -Objekt darstellt.

Verwenden Sie das optionale Argument *Quelle* zum Angeben einer Datenquelle mit einer der folgenden: ein **Command** -Objektvariable, eine SQL-Anweisung, eine gespeicherte Prozedur, ein Tabellenname, eine URL oder einen vollständigen Pfad Dateinamen. Wenn *Source* Pfadnamen einer Datei ist, kann ein vollständiger Pfad sein ("c:\\Dir\\file.rst"), ein relativer Pfad ("... \\file.rst "), oder eine URL ("https://files/file.rst").

Es ist nicht ratsam, verwenden Sie das Argument *Source* der **Open** -Methode eine Aktionsabfrage ausführen, die keine Datensätze zurückgegeben werden, da es keine einfache Möglichkeit ist, um festzustellen, ob der Aufruf erfolgreich war. Die von einer solchen Abfrage zurückgegebene **Recordset-Objekt** wird geschlossen. Rufen Sie die [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) -Methode eines **Command** -Objekts oder der [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) -Methode eines **Connection** -Objekts stattdessen um eine Abfrage durchzuführen, wie eine SQL-INSERT-Anweisung keine Datensätze zurückgegeben werden.

Das *ActiveConnection* -Argument entspricht der [ActiveConnection](activeconnection-property-ado.md) -Eigenschaft und gibt an, in welche Verbindung zum Öffnen des **Recordset** -Objekt. Wenn Sie eine Verbindungsdefinition für dieses Argument übergeben, öffnet ADO mithilfe der angegebenen Parameter eine neue Verbindung. Nach dem Öffnen des **Recordset-Objekt** mit einem clientseitige Cursor (**CursorLocation** = **AdUseClient**), können Sie den Wert dieser Eigenschaft zum Senden von Updates auf einen anderen Anbieter ändern. Sie können diese Eigenschaft auch auf **Nothing** (in Microsoft Visual Basic) oder NULL festlegen, um das **Recordset** -Objekt von beliebigen Anbietern zu trennen. Beim Ändern von **ActiveConnection** für einen serverseitigen Cursor wird jedoch ein Fehler generiert.

Bei anderen Argumenten, die den Eigenschaften eines **Recordset**-Objekts direkt entsprechen (*Source*, *CursorType* und *LockType*) gestaltet sich die Beziehung zwischen den Argumenten und den Eigenschaften folgendermaßen:

  - Vor dem Öffnen des **Recordset** -Objekts ist die Eigenschaft schreibgeschützt.

  - Wenn Sie beim Ausführen der **Open** -Methode nicht die entsprechenden Argumente übergeben, werden die Einstellungen der Eigenschaft verwendet. Falls Sie ein Argument übergeben, überschreibt es die entsprechende Einstellung der Eigenschaft, und diese wird auf den Wert des Arguments aktualisiert.

  - Nach dem Öffnen des **Recordset** -Objekts sind diese Eigenschaften schreibgeschützt.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>ActiveConnection</STRONG> -Eigenschaft wird nur für <STRONG>Recordset</STRONG> -Objekte gelesen, deren <A href="source-property-ado-recordset.md">Source</A>-Eigenschaft auf ein gültiges <STRONG>Command</STRONG> -Objekt festgelegt ist. Dies gilt auch, wenn das <STRONG>Recordset</STRONG> -Objekt nicht geöffnet ist.</P>



Wenn Sie das Argument *Quelle* ein **Command** -Objekt übergeben und auch ein *ActiveConnection* -Argument übergeben, tritt ein Fehler auf. Die **ActiveConnection** -Eigenschaft des **Command** -Objekts muss bereits auf ein gültiges **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festgelegt sein.

Wenn Sie einen anderen Wert als ein **Command** -Objekt im Argument *Source* übergeben, können Sie das Argument *Options* verwenden, um die Auswertung des Arguments *Quelle* zu optimieren. Wenn das Argument *Options* nicht definiert ist, können die Leistung verringert, da ADO Aufrufe an den Anbieter zu ermitteln, ob das Argument eine SQL-Anweisung, eine gespeicherte Prozedur, eine URL oder ein Tabellenname ist treffen muss auftreten. Wenn Sie wissen, welche Art von *Datenquelle* verwenden, ADO direkt mit der relevante Code springen weist das Argument *Optionen* festlegen. Wenn das Argument *Options* nicht *der Quelltyp* entspricht, tritt ein Fehler auf.

Wenn Sie das Argument *Source* ein **Stream** -Objekt übergeben, sollten Sie keine Informationen in die anderen Argumente übergeben. Andernfalls wird ein Fehler generiert. Die Informationen von **ActiveConnection** werden nicht aufbewahrt, wenn ein **Recordset** -Objekt aus einem **Stream** -Objekt geöffnet wird.

Der Standardwert für das Argument *Options* ist **AdCmdFile** , wenn keine Verbindung mit dem **Recordset-Objekt**zugeordnet ist. Dies ist in der Regel bei dauerhaft gespeicherten **Recordset** -Objekten der Fall.

Gibt die Datenquelle keine Datensätze zurück, legt der Anbieter die Eigenschaften [BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) auf **True** fest, und die Position des aktuellen Datensatzes ist nicht definiert. Sie können diesem leeren **Recordset** -Objekt dennoch Daten hinzufügen, sofern der Cursortyp dies zulässt.

Wenn Sie die Vorgänge für ein offenes **Recordset**-Objekt beendet haben, verwenden Sie die [Close](close-method-ado.md)-Methode, um alle zugeordneten Systemressourcen freizugeben. Ein Objekt wird beim Schließen nicht aus dem Speicher entfernt. Sie können dessen Eigeschaftseinstellungen ändern und es mithilfe der **Open**-Methode zu einem späteren Zeitpunkt erneut öffnen. Wenn Sie ein Objekt vollständig aus dem Speicher entfernen möchten, legen Sie die Objektvariable auf *Nothing* fest.

Bevor Sie die **ActiveConnection** -Eigenschaft festgelegt ist, rufen Sie **Open** ohne Operanden zum Erstellen einer Instanz eines **Recordset-Objekt** erstellt, indem Felder zur **Recordset** [Fields](fields-collection-ado.md) -Auflistung angehängt.

Wenn Sie die [CursorLocation](cursorlocation-property-ado.md) -Eigenschaft auf **AdUseClient**festgelegt haben, können Sie Zeilen in einem der folgenden beiden Methoden asynchron abrufen. Die empfohlene Methode ist für *Optionen* festzulegen, **AdAsyncFetch**. Alternativ können Sie die dynamische Eigenschaft "Asynchrone Rowset Verarbeitung" in der [Properties](properties-collection-ado.md) -Auflistung, aber verwandten abgerufenen Ereignisse können deshalb verloren gehen, wenn Sie nicht den **Options** -Parameter auf **AdAsyncFetch**festlegen.


> [!NOTE]
> <P>Abrufen der Hintergrund im MS Remote Provider wird nur über die <STRONG>Open</STRONG> -Methode <EM>Options</EM> -Parameter unterstützt.</P>


> [!NOTE]
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).


