---
title: Visual C++-ADO-Programmierung
TOCTitle: Visual C++ ADO Programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 660ae5523d3f04e7c533508e6c138b0f52d215c4
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937246"
---
# <a name="visual-c-ado-programming"></a>Visual C++-ADO-Programmierung


**Betrifft**: Access 2013, Office 2013

In der ADO-API-Referenz wird die Funktionalität der ADO-Anwendungsprogrammierschnittstelle (Application Programming Interface, API) mit einer Microsoft Visual Basic ähnlichen Syntax beschrieben. Obwohl die Zielgruppe alle Benutzer sind, verwendet ADO-Programmierer verschiedene Sprachen wie Visual Basic, Visual C++ (mit und ohne die ** \#importieren** Richtlinie), und Visual J++ (mit dem ADO/WFC-Klasse-Paket).

Um dieser Vielfalt gerecht zu werden, bieten die [ADO für Visual C++-Syntaxindizes](using-ado-with-microsoft-visual-c.md) eine Visual C++-sprachspezifische Syntax mit Verknüpfungen zu allgemeinen Beschreibungen der Funktionalität, der Parameter, außergewöhnlichen Verhaltensweisen usw. in der API-Referenz.

ADO wird mit COM-Schnittstellen (Component Object Model) implementiert. In bestimmten Programmiersprachen ist es jedoch einfacher für Programmierer mit COM zu arbeiten als in anderen. Beispielsweise werden nahezu alle Details der Verwendung von COM implizit für Visual Basic-Programmierer behandelt, wohingegen Visual C++-Programmierer die Details selbst ermitteln müssen.

In den folgenden Abschnitten werden Details für C und C++-Programmierer verwenden von ADO zusammengefasst und die ** \#importieren** Richtlinie. Der Schwerpunkt liegt auf den speziellen Datentypen für COM (**Variant**, **BSTR**und **SafeArray**) und Fehlerbehandlung (\_com\_Fehler).

## <a name="using-the-import-compiler-directive"></a>Mithilfe der \#-Compilerdirektive importieren

Die ** \#importieren** Visual C++-Compilerdirektive vereinfacht die Arbeit mit der ADO-Methoden und Eigenschaften. Die Richtlinie akzeptiert den Namen einer Datei mit einer Typbibliothek, wie der ADO-DLL (Msado15.dll), und generiert Headerdateien mit Typedef-Deklarationen, intelligente Zeiger für Schnittstellen und aufgezählte Konstanten. Jede Schnittstelle ist gekapselte oder eingebunden, in einer Klasse.

Für jeden Vorgang in einer Klasse (also ein Methoden- oder Eigenschaftenaufruf) gibt es eine Deklaration, um den Vorgang direkt aufzurufen (also die "Rohform" des Vorgangs), und eine Deklaration, um den Rohvorgang aufzurufen und einen COM-Fehler auszulösen, wenn der Vorgang nicht erfolgreich ausgeführt wird. Wenn es sich bei dem Vorgang um eine Eigenschaft handelt, wird normalerweise mit einer Compilerdirektive eine alternative Syntax für den Vorgang erstellt, die der Syntax von Visual Basic ähnelt.

Vorgänge, die den Wert einer Eigenschaft abzurufen, weisen Namen des Formulars, **Abrufen *** Eigenschaft*. Vorgänge, die den Wert einer Eigenschaft festgelegt haben Namen des Formulars, **platzieren *** Eigenschaft*. Vorgänge, die den Wert einer Eigenschaft mit einem Zeiger auf ein ADO-Objekt festgelegt haben Namen des Formulars, **PutRef *** Eigenschaft*.

Sie können eine Eigenschaft mit Aufrufen in der folgenden Form abrufen oder festlegen:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Verwenden von Eigenschaftendirektiven

Die ** \_ \_declspec(property...)** -Compilerdirektive ist eine Erweiterung der Microsoft-spezifischen C-Sprache, die eine Funktion, die als eine Eigenschaft verwendet, um eine alternative Syntax deklariert. Daher können Sie festlegen oder Abrufen von Werten einer Eigenschaft so ähnlich zu Visual Basic. Beispielsweise können Sie festlegen und Abrufen eine Eigenschaft auf diese Weise:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Der Code muss nicht wie folgt aussehen:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

Der Compiler generiert den entsprechenden **Get ***-*, **Put**-, oder **PutRef *** Eigenschaft* Anruf basierend auf welche alternative Syntax deklariert ist, und gibt an, ob die Eigenschaft wird gelesenen oder geschriebenen.

Die ** \_ \_declspec(property...)** -Compilerdirektive kann nur **get**, **put**oder **get** und **put** alternative Syntax für eine Funktion deklarieren. Schreibgeschützte Vorgänge weisen lediglich eine Erklärung **erhalten möchten** . lesegeschützte Vorgänge weisen lediglich eine Erklärung **zu platzieren** . Vorgänge, die Lese- und Schreibvorgang sind verfügen sowohl **get** und **put** -Deklarationen.

Es sind nur zwei Deklarationen mit dieser Richtlinie möglich. Jede Eigenschaft kann jedoch drei Eigenschaftenfunktionen haben: **Abrufen *** Eigenschaft*, **zu platzieren *** Eigenschaft*, und **PutRef *** Eigenschaft*. In diesem Fall weisen nur zwei Formen der Eigenschaft die alternative Syntax.

Beispielsweise wird der **ActiveConnection** -Eigenschaft für das **Command** -Objekt mit einer alternativen Syntax für deklariert **Abrufen *** ActiveConnection* und **PutRef *** ActiveConnection*. Die **PutRef**- Syntax ist eine gute Wahl, da in der Praxis Sie in der Regel werden ein geöffnetes **Connection** -Objekt (d. h., ein **Connection** -Objektzeiger) in dieser Eigenschaft aufnehmen möchten. Andererseits, hat das **Recordset** -Objekt **Abrufen**-, **Put**-, und **PutRef *** ActiveConnection* Vorgänge, aber keine alternative Syntax.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Auflistungen, GetItem-Methode und Item-Eigenschaft

ADO definiert mehrere Auflistungen, einschließlich **Fields**, **Parameters**, **Properties** und **Errors**. In Visual C++ gibt die **GetItem(***index***)**-Methode ein Member der Auflistung zurück. *Index* ist ein **Variant**-Wert, der eigentliche Wert ist ein numerischer Index des Members in der Auflistung oder eine Zeichenfolge mit dem Namen des Members.

Die ** \_ \_declspec(property...)** -Compilerdirektive deklariert die **Item** -Eigenschaft als eine alternative Syntax für jede Auflistung grundlegende **'GetItem()'** -Methode. Für die alternative Syntax werden eckige Klammern verwendet, und sie ähnelt einem Arrayverweis. Im Allgemeinen sehen die beiden Formen wie folgt aus:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Ein Feld eines **Recordset** -Objekts, mit dem Namen ***Rs***, abgeleitet aus der **Authors** -Tabelle der **Pubs** -Datenbank beispielsweise weisen Sie einen Wert zu. Verwenden Sie die Eigenschaft **Item()** Zugriff auf das dritte **Feld** der **Fields** -Auflistung des **Recordset** -Objekts (Sammlungen von 0 indiziert werden, sofern das dritte Feld den Namen ***au\_Fname***). Rufen Sie dann die **Value()** -Methode für das **Field** -Objekt einen String-Wert zuweisen.

Dies kann in Visual Basic auf die folgenden vier Arten ausgedrückt werden (die beiden letzten Formen gelten nur für Visual Basic, in anderen Sprachen gibt es keine Entsprechungen):

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

Die Entsprechung in Visual C++ zu den ersten beiden Formen lautet:

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-oder -(die alternative Syntax für die **Value** -Eigenschaft wird ebenfalls dargestellt)

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>COM-spezifische Datentypen

Im Allgemeinen weisen alle Visual Basic-Datentypen, die Sie in der ADO-API-Referenz finden, eine Visual C++-Entsprechung auf. Dazu gehören Standarddatentypen wie **unsigned char** für **Byte** in Visual Basic, **short** für **Integer** und **long** für **Long**. Mithilfe der Syntaxindizes können Sie genau feststellen, was für die Operanden einer bestimmten Methode oder Eigenschaft erforderlich ist.

Ausnahmen zu dieser Regel bilden die Datentypen, die nur für COM gelten: **Variant**, **BSTR** und **SafeArray**.

## <a name="variant"></a>Variant

Variant ist ein strukturierter Datentyp, der ein Wertmember und ein Datentypmember enthält. Ein Variant-Wert kann eine Vielzahl anderen Datentypen enthalten, u. a. einen anderen Variant-Wert, einen BSTR- oder Boolean-Wert, einen IDispatch- oder IUnknown-Zeiger, eine Währung und ein Datum. COM bietet außerdem Methoden, die die Konvertierung von Datentypen vereinfachen.

Die ** \_Variant\_t** -Klasse kapselt und verwaltet den **Variant** -Datentyp.

Wenn der ADO-API-Referenz besagt, eine Methode dass oder Operanden Eigenschaft einen Wert übernimmt, sie in der Regel bedeutet, dass übergebene Wert ist eine ** \_Variant\_t**.

Diese Regel ist explizit True, wenn der ADO-API-Referenz in den Themen im Abschnitt **Parameter** besagt, einen Operand dass **Variant**. Eine Ausnahme ist, wenn die Dokumentation ausdrücklich darauf hinweist, dass der Operand einen standard-Datentyp, wie **lange** oder **Byte**oder eine Enumeration übernimmt. Eine weitere Ausnahme ist, wenn der Operand eine **Zeichenfolge**akzeptiert.

## <a name="bstr"></a>BSTR

**BSTR** (**B**asic **STR**ing) ist ein strukturierter Datentyp, der eine Zeichenfolge und die Länge der Zeichenfolge enthält. COM bietet Methoden zum Zuordnen, Ändern und Freigeben eines **BSTR**-Werts.

Die ** \_Bstr\_t** -Klasse kapselt und verwaltet den **BSTR** -Datentyp.

Wenn der ADO-API-Referenz besagt, eine Methode dass oder Eigenschaft einen **String** -Wert übernimmt, bedeutet der Wert wird in Form von einer ** \_Bstr\_t**.

## <a name="casting-variantt-and-bstrt-classes"></a>Umwandeln von \_Variant\_t und \_Bstr\_t-Klassen

Häufig ist es nicht erforderlich, explizit Code eine ** \_Variant\_t** oder ** \_Bstr\_t** als Argument für einen Vorgang. Wenn die ** \_Variant\_t** oder ** \_Bstr\_t** Klasse hat einen Konstruktor, der den Datentyp des Arguments entspricht, und klicken Sie dann der Compiler generiert den entsprechenden ** \_Variant\_t** oder ** \_ BSTR\_t**.

Wenn das Argument jedoch nicht eindeutig ist, wenn also der Datentyp des Arguments mit mehr als einem Konstruktor übereinstimmt, müssen Sie das Argument mit dem entsprechenden Datentyp umwandeln, um den richtigen Konstruktor aufzurufen.

Beispielsweise lautet die Deklaration für die **Recordset::Open** -Methode wie folgt:

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

Das ActiveConnection-Argument übernimmt einen Verweis auf ein ** \_Variant\_t**, den Sie als Verbindungszeichenfolge oder als Zeiger auf ein geöffnetes **Connection** -Objekt codieren können.

Die richtige ** \_Variant\_t** wird implizit konstruiert, wenn Sie eine Zeichenfolge, z. B. übergeben "DSN = Pubs; Uid = sa; Pwd =;", oder einen Zeiger wie "(IDispatch \*) pConn".

Oder Sie können explizit code eine ** \_Variant\_t** mit einem Zeiger wie "\_Variant-Wert\_t ((IDispatch \*) pConn, true)". Die Cast (IDispatch \*), wird die Mehrdeutigkeit mit einem anderen Konstruktor, der einen Zeiger auf eine IUnknown-Schnittstelle akzeptiert aufgelöst.

Eine wichtige, aber selten erwähnte Tatsache ist, dass ADO eine IDispatch-Schnittstelle ist. Wenn ein Zeiger auf ein ADO-Objekt als ein Variant-Wert übergeben werden muss, muss dieser Zeiger als ein Zeiger auf eine IDispatch-Schnittstelle umgewandelt werden.

Im letzte Fall codes explizit das zweite boolesche Argument des Konstruktors mit dem optional, Standardwert true. Dieses Argument wird vom **Variant** Konstruktor rufen Sie die **AddRef**-Methode () dafür, dass von ADO automatisch die ** \_Variant\_t::Release**()-Methode, wenn der ADO-Methode oder Eigenschaft Aufruf abgeschlossen ist.

## <a name="safearray"></a>SafeArray

**SafeArray** ist ein strukturierter Datentyp, der ein Array anderer Datentypen enthält. **SafeArray** ist *sicherer* bezeichnet, da sie Informationen zu den Grenzen der einzelnen Arraydimension und schränkt den Zugriff auf Elemente innerhalb dieser Grenzen Arrays enthält.

Wenn in der ADO-API-Referenz angegeben ist, dass eine Methode oder Eigenschaft ein Array übernimmt oder zurückgibt, bedeutet dies, dass die Methode oder Eigenschaft einen **SafeArray** -Wert übernimmt oder zurückgibt, kein systemeigenes C/C++-Array.

Für den zweiten Parameter der **OpenSchema** -Methode des **Connection** -Objekts ist z. B. ein Array von **Variant** -Werten erforderlich. Diese **Variant** -Werte müssen als Elemente eines **SafeArray** -Werts übergeben werden, und dieser **SafeArray** -Wert muss als Wert eines anderen **Variant** -Werts festgelegt werden. Dieser andere **Variant** -Wert wird als zweites Argument von **OpenSchema** übergeben.

Als weiteres Beispiel ist das erste Argument der **Find** -Methode ein **Variant** -Wert, dessen Wert ein eindimensionaler **SafeArray** -Wert ist. Jedes optionale erste und zweite Argument von **AddNew** ist ein eindimensionaler **SafeArray** -Wert, und der Rückgabewert der **GetRows** -Methode ist ein **Variant** -Wert, dessen Wert ein zweidimensionaler **SafeArray** -Wert ist.

## <a name="missing-and-default-parameters"></a>Fehlende und Standardparameter

Bei Visual Basic sind fehlende Parameter in Methoden zulässig. Die **Open** -Methode des **Recordset** -Objekts weist z. B. fünf Parameter auf, aber Sie können Zwischenparameter überspringen und nachstehende Parameter auslassen. Ein standardmäßiger **BSTR** - oder **Variant** -Wert wird je nach Datentyp des fehlenden Operanden ersetzt.

In der C/C++ müssen alle Operanden angegeben werden. Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp eine Zeichenfolge ist, geben Sie eine ** \_Bstr\_t** mit einer leeren Zeichenfolge. Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp **Variant-Wert**ist, geben Sie eine ** \_Variant\_t** mit einem Wert von Verschiebung\_E\_PARAMNOTFOUND und einen Typ von VT\_Fehler. Alternativ angeben die Entsprechung ** \_Variant\_t** -Konstante, **VtMissing**, das von bereitgestellt wird die ** \#importieren** Richtlinie.

Drei Methoden bilden Ausnahmen zur üblichen Verwendung von **vtMissing**. Dies sind die **Execute** -Methoden der Objekte **Connection** - und **Command** -Objekte sowie die **NextRecordset** -Methode des **Recordset** -Objekts. Im Folgenden sind deren Signaturen aufgeführt:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Die Parameter *RecordsAffected* und *Parameters* sind Zeiger auf einen **Variant**-Wert. *Parameters* ist ein Eingabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, der einen Parameter oder ein Array von Parametern enthält, der bzw. das den ausgeführten Befehl ändert. *RecordsAffected* ist ein Ausgabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, an den die Anzahl der von der Methode betroffenen Zeilen zurückgegeben wird.

Geben Sie in das **Command** -Objekt **Execute** -Methode an, dass keine Parameter angegeben werden, indem Sie *Parameter* entweder \&VtMissing (was empfohlen wird) oder auf einen null-Zeiger (d. h., **NULL** oder 0 (null)). Wenn der *Parameter* auf null-Zeiger festgelegt ist, wird die Methode intern ersetzt das Äquivalent von **VtMissing**und schließt dann den Vorgang.

Geben Sie in den Methoden an, dass die Anzahl der betroffenen Datensätze nicht zurückgegeben werden soll, indem Sie *RecordsAffected* auf null-Zeiger festlegen. In diesem Fall ist der NULL-Zeiger kein fehlender Parameter, sondern ein Kennzeichen dafür, dass die Methode die Anzahl betroffener Datensätze verwerfen soll.

Deshalb können Sie für diese drei Methoden z. B. folgenden Code schreiben:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Fehlerbehandlung

In COM geben die meisten Vorgänge einen HRESULT-Rückgabecode, der angibt, ob eine Funktion erfolgreich abgeschlossen. Die ** \#importieren** Richtlinie generiert Wrappercode um jede "unformatierte" Methode oder Eigenschaft und überprüft den zurückgegebenen HRESULT. Wenn das HRESULT einen Fehler angibt, löst der Code einen COM-Fehler durch Aufrufen von \_com\_Problem\_errorex() mit dem HRESULT-Rückgabecode als Argument. Com-Error-Objekte abgefangen werden können, **versuchen Sie es**-**catch** -Block. (Aus Gründen der Effizienz catch einen Verweis auf ein ** \_com\_Fehler** -Objekt.)

Bedenken Sie, dass es sich dabei um ADO-Fehler handelt: Sie resultieren daraus, dass der ADO-Vorgang fehlschlägt. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekt angezeigt.

Die ** \#importieren** Richtlinie erstellt nur Fehler dadurch für Methoden und Eigenschaften, die in der ADO-DLL deklariert. Sie können jedoch den gleichen Mechanismus für die Fehlerbehandlung nutzen, indem Sie ein eigenes Makro oder eine Inlinefunktion für die Fehlerüberprüfung schreiben. Beispiele finden Sie im Thema [Visual C++-Erweiterungen](visual-c-extensions-for-ado.md) oder im Code in den folgenden Abschnitten.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Visual C++-Entsprechungen für Visual Basic-Konventionen

Im Folgenden finden Sie eine Zusammenfassung verschiedener Konventionen in der ADO-Dokumentation, codiert in Visual Basic, sowie deren Entsprechungen in Visual C++.

## <a name="declaring-an-ado-object"></a>Deklarieren eines ADO-Objekts

In Visual Basic wird eine ADO-Objektvariable (in diesem Fall für ein **Recordset** -Objekt) wie folgt deklariert:

```vb 
 
Dim rst As ADODB.Recordset 
```

Die Klausel "ADODB. Recordset-Objekt"ist die ProgID des **Recordset** -Objekts an, wie in der Registrierung definiert. Eine neue Instanz eines **Record** -Objekts wird wie folgt deklariert:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-oder -

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

In Visual C++ die ** \#importieren** Richtlinie generiert intelligente Zeiger-Typ-Deklarationen für alle ADO-Objekte. Beispielsweise eine Variable, die auf zeigt eine ** \_Recordset** -Objekt ist vom Typ ** \_RecordsetPtr**, und wird wie folgt deklariert:

```cpp 
 
_RecordsetPtr rs; 
```

Eine Variable, die auf eine neue Instanz des zeigt eine ** \_Recordset** Objekt wird wie folgt deklariert:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-oder -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-oder -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

Nachdem die **CreateInstance** -Methode aufgerufen wurde, kann die Variable wie folgt verwendet werden:

```cpp 
 
rs->Open(...); 
```

Beachten Sie, dass in einem Fall der "." Operator wird verwendet, als wäre der Variablen eine Instanz einer Klasse (Rs. CreateInstance), und in einem anderen Fall die "-\>" Operator wird verwendet, als wären die Variable einen Zeiger auf eine Schnittstelle (Rs -\>öffnen).

Eine Variable kann auf zwei Arten verwendet werden, da die "-\>" Operator wird überladen, um eine Instanz einer Klasse wie ein Zeiger auf eine Schnittstelle Verhalten kann. Mitglied private-Klasse die Instanzvariable enthält einen Zeiger auf die ** \_Recordset** Schnittstelle. die "-\>" Operator zurückgibt, Zeiger; und der zurückgegebene Zeiger greift auf die Mitglieder der ** \_Recordset** Objekt.

## <a name="coding-a-missing-parameter"></a>Codieren eines fehlenden Parameters - "Variant"

Wenn Sie einen fehlenden **String** -Operanden in Visual Basic codieren müssen, lassen Sie lediglich den Operanden aus. Sie müssen den Operanden in Visual C++ angeben. Code ein ** \_Bstr\_t** , die eine leere Zeichenfolge als Wert hat.

```cpp 
 
_bstr_t strMissing(L""); 
```

## <a name="coding-a-missing-parameter"></a>Codieren eines fehlenden Parameters - "Variant"

Wenn Sie einen fehlenden **Variant** Operanden in Visual Basic codieren müssen, lassen Sie lediglich den Operanden. Sie müssen alle Operanden in Visual C++ angeben. Codieren ein fehlenden Parameters **Variant-Wert** mit einer ** \_Variant\_t** legen Sie den speziellen Wert, Verschiebung\_E\_PARAMNOTFOUND und Typ, VT\_Fehler. Geben Sie alternativ **VtMissing**, die Entsprechung ist vordefinierte Konstante von bereitgestellt wird, die ** \#importieren** Richtlinie.

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-oder verwenden Sie-

```cpp 
 
...vtMissing...; 
```

## <a name="declaring-a-variant"></a>Deklarieren eines Variant-Werts

In Visual Basic wird ein **Variant** -Wert wie folgt mit der **Dim** -Anweisung deklariert:

```vb 
 
Dim VariableName As Variant 
```

Deklarieren Sie eine Variable als Typ in Visual C++ ** \_Variant\_t**. Einige schematische Darstellung ** \_Variant\_t** Deklarationen sind unten aufgeführt.


> [!NOTE]
> <P>[!HINWEIS] Diese Deklarationen geben Ihnen lediglich eine ungefähre Vorstellung davon, was Sie in Ihrem eigenen Programm codieren können. Weitere Informationen finden Sie in den Beispielen unten und in der Visual C++-Dokumentation.</P>



```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

## <a name="using-arrays-of-variants"></a>Verwenden von Arrays von Variant-Werten

In Visual Basic können Arrays von **Variant** -Werten mit der **Dim** -Anweisung codiert werden. Sie können dazu auch die **Array** -Funktion verwenden, wie im folgenden Beispielcode dargestellt:

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

Im folgenden Visual C++-Beispiel veranschaulicht die Verwendung von **SafeArray** mit verwendet eine ** \_Variant\_t**.


> [!NOTE]
> <P>[!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</P>



1.  Auch hier wird die TESTHR()-Inlinefunktion definiert, um den vorhandenen Mechanismus für die Fehlerbehandlung zu nutzen.

2.  Sie benötigen nur ein eindimensionales Array, sodass Sie **SafeArrayCreateVector** verwenden können, statt der allgemeinen **SAFEARRAYBOUND** -Deklaration und der **SafeArrayCreate** -Funktion. Der Code würde wie folgt aussehen, wenn **SafeArrayCreate** verwendet wird:
    
    ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
    ```

3.  Das Schema, identifiziert durch die enumerierte Konstante **AdSchemaColumns**, vier Einschränkungsspalten zugeordnet ist: Tabelle\_Katalog, Tabelle\_SCHEMA, Tabelle\_Namen und Spalte\_NAME. Aus diesem Grund wird ein Array von **Variant** -Werten mit vier Elementen erstellt. Klicken Sie dann einen Einschränkungswert, die die dritte Spalte, Tabelle entspricht\_NAME angegeben ist. Das **Recordset-Objekt** , das zurückgegeben wird besteht aus mehreren Spalten, die eine, die Teilmenge der Einschränkungsspalten ist. Die Werte der Einschränkungsspalten für jede Zeile zurückgegebene muss die entsprechende Einschränkungswerte identisch.

4.  Mit **SAFEARRAY** vertraut sind möglicherweise überrascht sein, dass **SafeArrayDestroy()** nicht vor dem Exit aufgerufen wird. Tatsächlich wird **SafeArrayDestroy()** Aufrufen in diesem Fall eine Laufzeit-Ausnahme ausgelöst. Der Grund dafür besteht darin, dass der Destruktor für VtCriteria soll ( **VariantClear aufgerufen werden**) Wenn der ** \_Variant\_t** wechselt außerhalb des Gültigkeitsbereichs, **SafeArray**freigegeben wird. Aufrufen von **SafeArrayDestroy**, ohne manuell löschen der ** \_Variant-Wert\_t**, würde den Destruktor versuchen, einen ungültigen **SafeArray** Zeiger zu löschen. Wenn **SafeArrayDestroy** aufgerufen wird, würde der Code wie folgt aussehen:
    
    ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
    ```
    
    Es ist jedoch viel einfacher, lassen Sie die ** \_Variant\_t** **SafeArray**verwalten.

<!-- end list -->

```cpp 
 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
#include <stdio.h> 
 
// Note 1 
inline void TESTHR( HRESULT _hr ) 
 { if FAILED(_hr) _com_issue_error(_hr); } 
 
void main(void) 
{ 
 CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 _ConnectionPtr pCn("ADODB.Connection"); 
 _variant_t vtTableName("authors"), 
 vtCriteria; 
 long ix[1]; 
 SAFEARRAY *pSa = NULL; 
 
 pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
 adConnectUnspecified); 
// Note 2, Note 3 
 pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
 if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
 
// Specify TABLE_NAME in the third array element (index of 2). 
 
 ix[0] = 2; 
 TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
 
// There is no Variant constructor for a SafeArray, so manually set the 
// type (SafeArray of Variant) and value (pointer to a SafeArray). 
 
 vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
 vtCriteria.parray = pSa; 
 
 pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
 
 long limit = pRs->GetFields()->Count; 
 for (long x = 0; x < limit; x++) 
 printf("%d: %s\n", x+1, 
 ((char*) pRs->GetFields()->Item[x]->Name)); 
// Note 4 
 pRs->Close(); 
 pCn->Close(); 
 } 
 catch (_com_error &e) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
 printf("Source = %s\n", (char*) e.Source()); 
 printf("Description = %s\n", (char*) e.Description()); 
 } 
 CoUninitialize(); 
} 
```

## <a name="using-property-getputputref"></a>Verwenden der Get/Put/PutRef-Eigenschaft

In Visual Basic wird der Name einer Eigenschaft nicht dadurch qualifiziert, ob sie abgerufen oder zugewiesen wird bzw. ob ihr ein Verweis zugewiesen wurde.

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

In diesem Visual C++-Beispiel wird gezeigt, **Abrufen**/**platzieren**/**PutRef *** Eigenschaft*.


> [!NOTE]
> [!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.



1.  In diesem Beispiel werden zwei Arten von einem fehlenden Zeichenfolgenargument: eine explizite Konstante, **StrMissing**und eine Zeichenfolge, die der Compiler erstellen einen temporären ** \_Bstr\_t** vorhanden, die für den Bereich der **Open** -Methode.

2.  Es ist nicht erforderlich, das Umwandeln des Operanden von Rs -\>PutRefActiveConnection(cn) an (IDispatch \*), da der Operand bereits ist (IDispatch \*).
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
    ```

## <a name="using-getitemx-and-itemx"></a>Mithilfe von "GetItem(x)" und "Item\[x\]

Mit diesem Visual Basic-Beispiel wird die standardmäßige und die alternative Syntax für **Item()** dargestellt.

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

Mit diesem Visual C++-Beispiel wird **Item** dargestellt.


> [!NOTE]
> <P>[!HINWEIS] Der folgende Hinweis entspricht kommentierten Abschnitten im Codebeispiel.</P>



1.  Wenn mit **Item** auf die Auflistung zugegriffen wird, muss der Index **2** in **long** umgewandelt werden, damit ein geeigneter Konstruktor aufgerufen wird.
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
    ```

## <a name="casting-ado-object-pointers-with-idispatch-"></a>Umwandeln von ADO-Objektzeigern mit "(IDispatch \*)"

Im folgenden Visual C++-Beispiel veranschaulicht die Verwendung (IDispatch \*) zu Cast ADO-Objektzeigern veranschaulicht.


> [!NOTE]
> <P>[!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.</P>



1.  Geben Sie ein geöffnetes **Connection** -Objekt in einer explizit codierten- **Variant**. Wandeln sie mit (IDispatch \*), damit der richtige Konstruktor aufgerufen wird. Auch explizit festlegen, die zweite ** \_Variant\_t** Parameter auf den Standardwert **true**, so dass der Referenzzähler Objekt am Ende des Vorgangs **Open** korrekt.

2.  Der Ausdruck (\_Bstr\_t), wird nicht umgewandelt, aber ein ** \_Variant-Wert\_t** Operator, der extrahiert ein ** \_Bstr\_t** Zeichenfolge aus der zurückgegebene **Wert** **Variant-Wert** . Der Ausdruck (Char\*), wird nicht umgewandelt, aber ein ** \_Bstr\_t** Operator, der einen Zeiger in die gekapselte Zeichenfolge in extrahiert ein ** \_Bstr\_t** Objekt. In diesem Abschnitt werden einige nützliche Verhaltensweisen von veranschaulicht ** \_Variant\_t** und ** \_Bstr\_t** Operatoren.
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
    ```

