---
title: Open-Methode (ADO-Recordset)
TOCTitle: Open method (ADO Recordset)
ms:assetid: 87ef19a4-28e1-dec7-ed33-4ae500b9c460
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249591(v=office.15)
ms:contentKeyID: 48546119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5f8dbdfa61a671e2efb9aac2596cfda5cd1727b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288406"
---
# <a name="open-method-ado-recordset"></a>Open-Methode (ADO-Recordset)

**Gilt für**: Access 2013, Office 2013

Öffnet einen Cursor.

## <a name="syntax"></a>Syntax

*Recordset*. Open*Source*, *ActiveConnection*, *CursorType*, *LockType*, *Optionen*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. Ein **Variant** -Wert, der ausgewertet ein gültiges [Command](command-object-ado.md)-Objekt, eine SQL-Anweisung, einen Tabellennamen, den Aufruf einer gespeicherten Prozedur, eine URL oder den Namen einer Datei oder eines [Stream](stream-object-ado.md)-Objekts mit einem dauerhaft gespeicherten [Recordset](recordset-object-ado.md)-Objekt ergibt.|
|*ActiveConnection* |Optional. Ein **Variant** -Wert, der den Namen einer gültigen [Connection](connection-object-ado.md)-Objektvariablen ergibt, oder ein **String** -Wert, der [ConnectionString](connectionstring-property-ado.md)-Parameter enthält.|
|*CursorType* |Optional. Ein [CursorTypeEnum](cursortypeenum.md)-Wert, der den Cursortyp bestimmt, den der Anbieter zum Öffnen des **Recordset** -Objekts verwenden soll. Der Standardwert ist **adOpenForwardOnly**.|
|*LockType* |Optional. Ein [LockTypeEnum](locktypeenum.md)-Wert, der den Sperrtyp (vollständige Parallelität) bestimmt, den der Anbieter zum Öffnen des **Recordset** -Objekts verwenden sollte. Der Standardwert lautet **adLockReadOnly**.|
|*Options* |Optional. Ein **Long**-Wert, der angibt, wie der Anbieter das Argument *Source* auswerten sollte, wenn es ein anderes Element als ein **Command**-Objekt darstellt, oder dass das **Recordset**-Objekt aus einer Datei wiederhergestellt werden sollte, in der es zuvor gespeichert wurde. Es kann sich um einen oder mehrere [CommandTypeEnum](commandtypeenum.md)-Werte oder [ExecuteOptionEnum](executeoptionenum.md)-Werte handeln, die mit einem bitweisen AND-Operator kombiniert werden können.|

> [!NOTE]
> [!HINWEIS] Wenn Sie ein **Recordset** -Objekt aus einem **Stream** -Objekt, das ein permanentes **Recordset** -Objekt enthält, mithilfe eines **ExecuteOptionEnum** -Werts **adAsyncFetchNonBlocking** öffnen, hat dies keine Auswikungen. Der Abruf ist synchron und blockierend.

Die **ExecuteOpenEnum**-Werte für **adExecuteNoRecords** oder **adExecuteStream** sollten nicht mit **Open** verwendet werden.

## <a name="remarks"></a>Bemerkungen

Bei dem Standardcursor für ein **Recordset**-Objekt in ADO handelt es sich um einen vorwärtsgerichteten, schreibgeschützten Cursor, der sich auf dem Server befindet.

Mithilfe der **Open** -Methode für ein **Recordset** -Objekt können Sie einen Cursor öffnen, der Datensätze aus einer Basistabelle, die Ergebnisse einer Abfrage oder ein zuvor gespeichertes **Recordset** -Objekt darstellt.

Verwenden Sie ein optionales Argument *Source*, um eine Datenquelle mithilfe eines der folgenden Elementen anzugeben: eine **Command**-Objektvariable, eine SQL-Anweisung, eine gespeicherte Prozedur, einen Tabellennamen, eine URL oder den vollständigen Pfadnamen einer Datei. Wenn *Source* ein Dateipfad ist, kann dies ein vollständiger Pfad ("c:\\dir\\file. RST"), ein relativer Pfad (".. \\") oder eine URL ("https://files/file.rst").

Es ist nicht empfehlenswert, das Argument *Source* der **Open**-Methode zu verwenden, um eine Aktionsabfrage durchzuführen, bei der keine Datensätze zurückgegeben werden, da nur schwer festgestellt werden kann, ob der Aufruf erfolgreich war. Das bei einer solchen Abfrage zurückgegebene **Recordset**-Objekt wird geschlossen. Rufen Sie die [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)-Methode eines **Command**-Objekts oder die [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)-Methode eines **Connection**-Objekts auf, anstatt eine Abfrage durchzuführen, bei der keine Datensätze zurückgegeben werden (z. B. eine SQL-INSERT-Anweisung).

Das Argument *ActiveConnection* entspricht der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft und gibt an, in welcher Verbindung das **Recordset**-Objekt geöffnet werden soll. Wenn Sie eine Verbindungsdefinition für dieses Argument übergeben, öffnet ADO mithilfe der angegebenen Parameter eine neue Verbindung. Nach dem Öffnen **des Recordset-Objekts** mit einem clientseitigen Cursor (**CursorLocation** = **adUseClient**) können Sie den Wert dieser Eigenschaft ändern, um Aktualisierungen an einen anderen Anbieter zu senden. Sie können diese Eigenschaft auch auf **Nothing** (in Microsoft Visual Basic) oder NULL festlegen, um das **Recordset** -Objekt von beliebigen Anbietern zu trennen. Beim Ändern von **ActiveConnection** für einen serverseitigen Cursor wird jedoch ein Fehler generiert.

Bei anderen Argumenten, die den Eigenschaften eines **Recordset**-Objekts direkt entsprechen (*Source*, *CursorType* und *LockType*) gestaltet sich die Beziehung zwischen den Argumenten und den Eigenschaften folgendermaßen:

- Vor dem Öffnen des **Recordset**-Objekts ist die Eigenschaft schreibgeschützt.

- Wenn Sie beim Ausführen der **Open** -Methode nicht die entsprechenden Argumente übergeben, werden die Einstellungen der Eigenschaft verwendet. Falls Sie ein Argument übergeben, überschreibt es die entsprechende Einstellung der Eigenschaft, und diese wird auf den Wert des Arguments aktualisiert.

- Nach dem Öffnen des **Recordset** -Objekts sind diese Eigenschaften schreibgeschützt.

> [!NOTE]
> Die **ActiveConnection**-Eigenschaft wird nur für **Recordset**-Objekte gelesen, deren [Source](source-property-ado-recordset.md)-Eigenschaft auf ein gültiges **Command**-Objekt festgelegt ist. Dies gilt auch, wenn das **Recordset**-Objekt nicht geöffnet ist.

Wenn Sie ein **Command**-Objekt in einem Argument *Source* und gleichzeitig ein Argument *ActiveConnection* übergeben, tritt ein Fehler auf. Die **ActiveConnection**-Eigenschaft des **Command**-Objekts muss bereits auf ein gültiges **Connection**-Objekt oder eine gültige Verbindungszeichenfolge festgelegt sein.

Wenn Sie im Argument *Source* statt einem **Command**-Objekt ein anderes Element übergeben, können Sie das Argument *Options* verwenden, um die Analyse des Arguments *Source* zu optimieren. Ist das Argument *Options* nicht definiert, stellen Sie möglicherweise fest, dass sich die Leistung verringert, da ADO Aufrufe an den Anbieter vornehmen muss, um zu bestimmen, ob es sich bei dem Argument um eine SQL-Anweisung, eine gespeicherte Prozedur, eine URL oder einen Tabellennamen handelt. Wenn Ihnen bekannt ist, welchen *Source*-Typ Sie verwenden, können Sie das Argument *Options* festlegen, damit ADO direkt zum nächsten relevanten Code wechselt. Stimmt das Argument *Options* nicht mit dem *Source*-Typ überein, tritt ein Fehler auf.

Wenn Sie ein **Stream**-Objekt in das Argument *Source* übergeben, sollten Sie keine Informationen in die anderen Argumente übergeben. Andernfalls wird ein Fehler generiert. Die Informationen von **ActiveConnection** werden nicht aufbewahrt, wenn ein **Recordset**-Objekt aus einem **Stream**-Objekt geöffnet wird.

Wenn dem **Recordset**-Objekt keine Verbindung zugeordnet ist, lautet der Standardwert für das Argument *Options ***adCmdFile**. Dies ist in der Regel bei dauerhaft gespeicherten **Recordset**-Objekten der Fall.

Gibt die Datenquelle keine Datensätze zurück, legt der Anbieter die Eigenschaften [BOF](bof-eof-properties-ado.md) und [EOF](bof-eof-properties-ado.md) auf **True** fest, und die Position des aktuellen Datensatzes ist nicht definiert. Sie können diesem leeren **Recordset** -Objekt dennoch Daten hinzufügen, sofern der Cursortyp dies zulässt.

Wenn Sie die Vorgänge für ein offenes **Recordset**-Objekt beendet haben, verwenden Sie die [Close](close-method-ado.md)-Methode, um alle zugeordneten Systemressourcen freizugeben. Ein Objekt wird beim Schließen nicht aus dem Speicher entfernt. Sie können dessen Eigeschaftseinstellungen ändern und es mithilfe der **Open**-Methode zu einem späteren Zeitpunkt erneut öffnen. Wenn Sie ein Objekt vollständig aus dem Speicher entfernen möchten, legen Sie die Objektvariable auf *Nothing* fest.

Bevor die **ActiveConnection** -Eigenschaft festgelegt wird, rufen Sie **Open** ohne Operanden auf, um eine Instanz eines **Recordset** -Objekts zu erstellen, das durch Anfügen von Feldern an die **Recordset** [Fields](fields-collection-ado.md) -Auflistung erstellt wird.

Wenn Sie die [CursorLocation](cursorlocation-property-ado.md) -Eigenschaft auf **adUseClient**festgelegt haben, können Sie Zeilen asynchron auf eine von zwei Arten abrufen. Die empfohlene Methode besteht darin, *Optionen* auf **adAsyncFetch**festzulegen. Alternativ können Sie die dynamische Eigenschaft "asynchrone Rowset-Verarbeitung" in der [Properties](properties-collection-ado.md) -Auflistung verwenden, aber zugehörige abgerufene Ereignisse können verloren gehen, wenn Sie den **options** -Parameter nicht auf **adAsyncFetch**festlegen.

> [!NOTE]
> Das Abrufen im Hintergrund wird im Microsoft OLE DB-Anbieter für Remoting nur durch den *Options*-Parameter der **Open**-Methode unterstützt.

> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [absolute und relative URLs](absolute-and-relative-urls.md).


