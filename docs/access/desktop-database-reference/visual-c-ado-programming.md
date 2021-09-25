---
title: Visual C++ ADO-Programmierung
TOCTitle: Visual C++ ADO programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 424a5548f79f42a8d0993c96a946c4636ae093b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572550"
---
# <a name="visual-c-ado-programming"></a>Visual C++ ADO-Programmierung

**Gilt für**: Access 2013, Office 2013

In der ADO-API-Referenz wird die Funktionalität der ADO-Anwendungsprogrammierschnittstelle (Application Programming Interface, API) mit einer Microsoft Visual Basic ähnlichen Syntax beschrieben. Obwohl die Zielgruppe alle Benutzer sind, verwenden ADO-Programmierer verschiedene Sprachen wie Visual Basic, Visual C++ (mit und ohne **\# Importdirektive)** und Visual J++ (mit dem ADO/WFC-Klassenpaket).

Um dieser Vielfalt gerecht zu werden, bieten die [ADO für Visual C++-Syntaxindizes](using-ado-with-microsoft-visual-c.md) eine Visual C++-sprachspezifische Syntax mit Verknüpfungen zu allgemeinen Beschreibungen der Funktionalität, der Parameter, außergewöhnlichen Verhaltensweisen usw. in der API-Referenz.

ADO wird mit COM-Schnittstellen (Component Object Model) implementiert. In bestimmten Programmiersprachen ist es jedoch einfacher für Programmierer mit COM zu arbeiten als in anderen. Beispielsweise werden nahezu alle Details der Verwendung von COM implizit für Visual Basic-Programmierer behandelt, wohingegen Visual C++-Programmierer die Details selbst ermitteln müssen.

In den folgenden Abschnitten werden Details für C- und C++-Programmierer zusammengefasst, die ADO und die **\# Importdirektive verwenden.** Der Schwerpunkt liegt auf comspezifischen Datentypen (**Variant**, **BSTR** und **SafeArray**) und der Fehlerbehandlung ( \_ com \_ error).

## <a name="using-the-import-compiler-directive"></a>Verwenden der \# Importcompilerdirektive

Die Visual C++-Compilerdirektive **\# zum Importieren** vereinfacht das Arbeiten mit den ADO-Methoden und -Eigenschaften. The directive takes the name of a file containing a type library, such as the ADO .dll (Msado15.dll), and generates header files containing typedef declarations, smart pointers for interfaces, and enumerated constants. Each interface is encapsulated, or wrapped, in a class.

Für jeden Vorgang in einer Klasse (also ein Methoden- oder Eigenschaftenaufruf) gibt es eine Deklaration, um den Vorgang direkt aufzurufen (also die "Rohform" des Vorgangs), und eine Deklaration, um den Rohvorgang aufzurufen und einen COM-Fehler auszulösen, wenn der Vorgang nicht erfolgreich ausgeführt wird. Wenn es sich bei dem Vorgang um eine Eigenschaft handelt, wird normalerweise mit einer Compilerdirektive eine alternative Syntax für den Vorgang erstellt, die der Syntax von Visual Basic ähnelt.

Vorgänge, von denen der Wert einer Eigenschaft abgerufen wird, weisen Namen in der folgenden Form auf: **Get**_Property_. Vorgänge, von denen der Wert einer Eigenschaft festgelegt wird, weisen Namen in der folgenden Form auf: **Put**_Property_. Vorgänge, von denen der Wert einer Eigenschaft mit einem Zeiger auf ein ADO-Objekt festgelegt wird, weisen Namen in der folgenden Form auf: **PutRef**_Property_.

Sie können eine Eigenschaft mit Aufrufen in der folgenden Form abrufen oder festlegen:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Verwenden von Eigenschaftsdirektiven

Die Compilerdirektive **\_ \_ declspec(property...)** ist eine Microsoft-spezifische C-Spracherweiterung, die eine Funktion deklariert, die als Eigenschaft mit einer alternativen Syntax verwendet wird. Daher können Sie Werte einer Eigenschaft ähnlich wie bei Visual Basic festlegen oder abrufen. Sie können z. B. wie folgt eine Eigenschaft festlegen und abrufen:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Der Code muss nicht wie folgt aussehen:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

Der Compiler generiert den entsprechenden _-_ Get-, **Put-oder**_PutRef-Eigenschaftsaufruf_ basierend darauf, welche alternative Syntax deklariert wird und ob die Eigenschaft gelesen oder geschrieben wird. 

Die compilerdirektive **\_ \_ declspec(property...)** kann nur **"get",** **"put"** oder **"get"** deklarieren und alternative Syntax für eine Funktion **festlegen.** Schreibgeschützte Vorgänge verfügen  nur über eine Get-Deklaration. Schreibgeschützte Vorgänge verfügen  nur über eine Put-Deklaration. Vorgänge, bei denen sowohl Lese- als auch Schreibvorgänge ausgeführt werden, verfügen über **get-** und put-Deklarationen. 

Für diese Direktive sind nur zwei Deklarationen möglich. Jede Eigenschaft kann jedoch drei Eigenschaftenfunktionen aufweisen: **Get**_Property_, **Put**_Property_ und **PutRef**_Property_. In diesem Fall weisen nur zwei Formen der Eigenschaft die alternative Syntax auf.

Beispielsweise wurde die **ActiveConnection**-Eigenschaft des **Command**-Objekts mit einer alternativen Syntax für **Get**_ActiveConnection_ und **PutRef**_ActiveConnection_ deklariert. Die **PutRef**-Syntax ist eine gute Wahl, weil Sie in der Praxis üblicherweise in diese Eigenschaft ein offenes **Connection**-Objekt aufnehmen (d. h. einen **Connection**-Objektzeiger). Andererseits weist das **Recordset**-Objekt **Get**-, **Put**- und **PutRef**_ActiveConnection_-Vorgänge auf, aber keine alternative Syntax.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Auflistungen, die GetItem-Methode und die Item-Eigenschaft

ADO definiert mehrere Auflistungen, einschließlich **Fields**, **Parameters**, **Properties** und **Errors**. In Visual C++ gibt die **GetItem(**_index_*_) -Methode_* ein Element der Auflistung zurück. *Index* ist ein **Variant**-Wert, der eigentliche Wert ist ein numerischer Index des Members in der Auflistung oder eine Zeichenfolge mit dem Namen des Members.

Die Compilerdirektive **\_ \_ declspec(property...)** deklariert die **Item-Eigenschaft** als alternative Syntax für die grundlegende **GetItem()-Methode** jeder Auflistung. Für die alternative Syntax werden eckige Klammern verwendet, und sie ähnelt einem Arrayverweis. Im Allgemeinen sehen die beiden Formen wie folgt aus:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Weisen Sie beispielsweise einem Feld eines **Recordset-Objekts** mit dem Namen rs _einen Wert ***zu, der von der* _authors-Tabelle** der **Pubs-Datenbank** abgeleitet wird. Verwenden Sie die **Item()-Eigenschaft,** um auf  das dritte **Field-Objekt** der **Fields-Auflistung des Recordset-Objekts** zuzugreifen (Auflistungen werden von Null indiziert; angenommen, das dritte Feld heißt **_au \_ fname_*_). Rufen Sie dann die* _Value()-Methode** für das **Field-Objekt** auf, um einen Zeichenfolgenwert zuzuweisen.

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

\-oder- (die alternative Syntax für die **Value-Eigenschaft** ist ebenfalls dargestellt)

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>COM-spezifische Datentypen

Im Allgemeinen weisen alle Visual Basic-Datentypen, die Sie in der ADO-API-Referenz finden, eine Visual C++-Entsprechung auf. Dazu gehören Standarddatentypen wie **unsigned char** für **Byte** in Visual Basic, **short** für **Integer** und **long** für **Long**. Mithilfe der Syntaxindizes können Sie genau feststellen, was für die Operanden einer bestimmten Methode oder Eigenschaft erforderlich ist.

Ausnahmen zu dieser Regel bilden die Datentypen, die nur für COM gelten: **Variant**, **BSTR** und **SafeArray**.

### <a name="variant"></a>Variant

A **Variant** is a structured data type that contains a value member and a data type member. A **Variant** may contain a wide range of other data types including another Variant, BSTR, Boolean, IDispatch or IUnknown pointer, currency, date, and so on. COM also provides methods that make it easy to convert one data type to another.

Die **\_ Variant \_ t-Klasse** kapselt und verwaltet den **Variant-Datentyp.**

Wenn die ADO-API-Referenz besagt, dass eine Methode oder ein Eigenschaftenopernd einen Wert akzeptiert, bedeutet dies in der Regel, dass der Wert in einer **\_ Variante \_ t** übergeben wird.

This rule is explicitly true when the **Parameters** section in the topics of the ADO API Reference says an operand is a **Variant**. One exception is when the documentation explicitly says the operand takes a standard data type, such as **Long** or **Byte**, or an enumeration. Another exception is when the operand takes a **String**.

### <a name="bstr"></a>BSTR

**BSTR** (**B** asic **STR** ing) ist ein strukturierter Datentyp, der eine Zeichenfolge und die Länge der Zeichenfolge enthält. COM bietet Methoden zum Zuordnen, Ändern und Freigeben eines **BSTR**-Werts.

Die **\_ bstr \_ t-Klasse** kapselt und verwaltet den **BSTR-Datentyp.**

Wenn die ADO-API-Referenz besagt, dass eine Methode oder Eigenschaft einen **String-Wert** annimmt, bedeutet dies, dass der Wert in Form einer **\_ bstr \_ t** ist.

#### <a name="casting-_variant_t-and-_bstr_t-classes"></a>\_Umwandlungsvariante \_ t- und \_ bstr \_ t-Klassen

Häufig ist es nicht erforderlich, eine **\_ Variante \_ t** oder **\_ bstr \_ t** in einem Argument explizit in einen Vorgang zu codieren. Wenn die **\_ Variant \_ t-** oder **\_ bstr \_ t-Klasse** über einen Konstruktor verfügt, der dem Datentyp des Arguments entspricht, generiert der Compiler die entsprechende **\_ Variante \_ t** oder **\_ bstr \_ t.**

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

The ActiveConnection argument takes a reference to a **\_ variant \_ t**, which you may code as a connection string or a pointer to an open **Connection** object.

Die richtige **\_ Variante \_ t** wird implizit konstruiert, wenn Sie eine Zeichenfolge wie "DSN=pubs;uid=sa;pwd=;" oder einen Zeiger wie "(IDispatch \* ) pConn" übergeben.

Sie können auch explizit eine Variante programmieren, **\_ \_ die keinen** Zeiger enthält, z. B. \_ "Variant \_ t((IDispatch \* ) pConn, true)". Die Umwandlung (IDispatch) \* löst die Zweideutigkeit mit einem anderen Konstruktor auf, der einen Zeiger auf eine IUnknown-Schnittstelle verwendet.

It is a crucial, though seldom mentioned fact, that ADO is an IDispatch interface. Whenever a pointer to an ADO object must be passed as a **Variant**, that pointer must be cast as a pointer to an IDispatch interface.

Im letzten Fall wird das zweite boolesche Argument des Konstruktors explizit mit dem optionalen Standardwert true codiert. Dieses Argument bewirkt, dass der **Variant-Konstruktor** seine **AddRef**()-Methode aufruft, wodurch ADO automatisch die **\_ Variant \_ t::Release**()-Methode aufruft, wenn der ADO-Methoden- oder -Eigenschaftsaufruf abgeschlossen ist.

### <a name="safearray"></a>Safearray

**SafeArray** ist ein strukturierter Datentyp, der ein Array anderer Datentypen enthält. **SafeArray** wird als *safe* (sicher) bezeichnet, da dieser Datentyp Informationen zu den Grenzen der einzelnen Arraydimensionen enthält und den Zugriff auf die Arrayelemente innerhalb dieser Grenzen beschränkt.

Wenn in der ADO-API-Referenz angegeben ist, dass eine Methode oder Eigenschaft ein Array übernimmt oder zurückgibt, bedeutet dies, dass die Methode oder Eigenschaft einen **SafeArray** -Wert übernimmt oder zurückgibt, kein systemeigenes C/C++-Array.

Für den zweiten Parameter der **OpenSchema** -Methode des **Connection** -Objekts ist z. B. ein Array von **Variant** -Werten erforderlich. Diese **Variant** -Werte müssen als Elemente eines **SafeArray** -Werts übergeben werden, und dieser **SafeArray** -Wert muss als Wert eines anderen **Variant** -Werts festgelegt werden. Dieser andere **Variant** -Wert wird als zweites Argument von **OpenSchema** übergeben.

Als weiteres Beispiel ist das erste Argument der **Find** -Methode ein **Variant** -Wert, dessen Wert ein eindimensionaler **SafeArray** -Wert ist. Jedes optionale erste und zweite Argument von **AddNew** ist ein eindimensionaler **SafeArray** -Wert, und der Rückgabewert der **GetRows** -Methode ist ein **Variant** -Wert, dessen Wert ein zweidimensionaler **SafeArray** -Wert ist.

## <a name="missing-and-default-parameters"></a>Fehlende und Standardparameter

Bei Visual Basic sind fehlende Parameter in Methoden zulässig. Die **Open** -Methode des **Recordset** -Objekts weist z. B. fünf Parameter auf, aber Sie können Zwischenparameter überspringen und nachstehende Parameter auslassen. Ein standardmäßiger **BSTR** - oder **Variant** -Wert wird je nach Datentyp des fehlenden Operanden ersetzt.

In C/C++, all operands must be specified. Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp eine Zeichenfolge ist, geben Sie einen **\_ bstr \_ t** an, der eine NULL-Zeichenfolge enthält. Wenn Sie einen fehlenden Parameter angeben möchten, dessen Datentyp ein **Variant-Datentyp** ist, geben Sie eine **\_ Variante \_ t** mit dem Wert DISP \_ E \_ PARAMNOTFOUND und einem VT \_ ERROR-Typ an. Alternativ können Sie die entsprechende **\_ Variant \_ t-Konstante** **vtMissing** angeben, die von der **\# Importdirektive** bereitgestellt wird.

Drei Methoden bilden Ausnahmen zur üblichen Verwendung von **vtMissing**. Dies sind die **Execute** -Methoden der Objekte **Connection** - und **Command** -Objekte sowie die **NextRecordset** -Methode des **Recordset** -Objekts. Im Folgenden sind deren Signaturen aufgeführt:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Die Parameter *RecordsAffected* und *Parameters* sind Zeiger auf einen **Variant**-Wert. *Parameters* ist ein Eingabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, der einen Parameter oder ein Array von Parametern enthält, der bzw. das den ausgeführten Befehl ändert. *RecordsAffected* ist ein Ausgabeparameter, mit dem die Adresse eines **Variant**-Werts angegeben wird, an den die Anzahl der von der Methode betroffenen Zeilen zurückgegeben wird.

In the **Command** object **Execute** method, indicate that no parameters are specified by setting *Parameters* to either \& vtMissing (which is recommended) or to the null pointer (that is, **NULL** or zero (0)). Wird *Parameters* auf einen NULL-Zeiger festgelegt, ersetzt die Methode intern die Entsprechung von **vtMissing** und schließt dann den Vorgang ab.

Geben Sie für alle Methoden an, dass die Anzahl betroffener Datensätze nicht zurückgegeben werden soll, indem Sie *RecordsAffected* auf den NULL-Zeiger festlegen. In diesem Fall ist der NULL-Zeiger kein fehlender Parameter, sondern ein Kennzeichen dafür, dass die Methode die Anzahl betroffener Datensätze verwerfen soll.

Deshalb können Sie für diese drei Methoden z. B. folgenden Code schreiben:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Fehlerbehandlung

In COM, most operations return an HRESULT return code that indicates whether a function completed successfully. Die **\# Importdirektive** generiert Wrappercode um jede "raw"-Methode oder -Eigenschaft und überprüft das zurückgegebene HRESULT. Wenn HRESULT einen Fehler angibt, löst der Wrappercode einen COM-Fehler aus, indem \_ com \_ issue \_ errorex() mit dem HRESULT-Rückgabecode als Argument aufgerufen wird. COM error objects can be caught in a **try**-**catch** block. (Um der Effizienz willen, fangen Sie einen Verweis auf ein **\_ \_ Com-Fehlerobjekt** ab.)

Bedenken Sie, dass es sich dabei um ADO-Fehler handelt: Sie resultieren daraus, dass der ADO-Vorgang fehlschlägt. Fehler, die vom zugrunde liegenden Anbieter zurückgegeben werden, werden als **Error** -Objekte in der **Errors** -Auflistung des **Connection** -Objekt angezeigt.

Die **\# Importdirektive** erstellt nur Fehlerbehandlungsroutinen für Methoden und Eigenschaften, die im ADO-.dll deklariert sind. Sie können jedoch den gleichen Mechanismus für die Fehlerbehandlung nutzen, indem Sie ein eigenes Makro oder eine Inlinefunktion für die Fehlerüberprüfung schreiben. Beispiele finden Sie im Thema [Visual C++-Erweiterungen](visual-c-extensions-for-ado.md) oder im Code in den folgenden Abschnitten.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Visual C++-Entsprechungen Visual Basic Konventionen

Im Folgenden finden Sie eine Zusammenfassung verschiedener Konventionen in der ADO-Dokumentation, codiert in Visual Basic, sowie deren Entsprechungen in Visual C++.

### <a name="declaring-an-ado-object"></a>Deklarieren eines ADO-Objekts

In Visual Basic wird eine ADO-Objektvariable (in diesem Fall für ein **Recordset** -Objekt) wie folgt deklariert:

```vb 
 
Dim rst As ADODB.Recordset 
```

Die Klausel " ADODB. Recordset" ist die ProgID des **Recordset-Objekts** gemäß der Definition in der Registrierung. Eine neue Instanz eines **Record** -Objekts wird wie folgt deklariert:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-oder-

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

In Visual C++ generiert die **\# Importdirektive** intelligente Zeigertypdeklarationen für alle ADO-Objekte. Beispielsweise ist eine Variable, die auf ein **\_ Recordset -Objekt** zeigt, vom Typ **\_ RecordsetPtr** und wird wie folgt deklariert:

```cpp 
 
_RecordsetPtr rs; 
```

Eine Variable, die auf eine neue Instanz eines **\_ Recordset-Objekts** verweist, wird wie folgt deklariert:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-oder-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-oder-

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

Nachdem die **CreateInstance** -Methode aufgerufen wurde, kann die Variable wie folgt verwendet werden:

```cpp 
 
rs->Open(...); 
```

Beachten Sie, dass in einem Fall der Operator "." verwendet wird, als wäre die Variable eine Instanz einer Klasse (rs. CreateInstance), und in einem anderen Fall wird der Operator "- \> " verwendet, als ob die Variable ein Zeiger auf eine Schnittstelle wäre (rs- \> Open).

Eine Variable kann auf zwei Arten verwendet werden, da der Operator "- \> " überladen ist, damit sich eine Instanz einer Klasse wie ein Zeiger auf eine Schnittstelle verhalten kann. Ein privates Klassenmitglied der Instanzvariablen enthält einen Zeiger auf die **\_ Recordset-Schnittstelle;** der Operator "- \> " gibt diesen Zeiger zurück, und der zurückgegebene Zeiger greift auf die Member des **\_ Recordset-Objekts** zu.

### <a name="coding-a-missing-parameter"></a>Codieren eines fehlenden Parameters

#### <a name="string"></a>Zeichenfolge

Wenn Sie einen fehlenden **String** -Operanden in Visual Basic codieren müssen, lassen Sie lediglich den Operanden aus. Sie müssen den Operanden in Visual C++ angeben. Codiert ein **\_ bstr t-Objekt \_** mit einer leeren Zeichenfolge als Wert.

```cpp 
 
_bstr_t strMissing(L""); 
```

#### <a name="variant"></a>Variant

When you need to code a missing **Variant** operand in Visual Basic, you merely omit the operand. You must specify all operands in Visual C++. Code a missing **Variant** parameter with a **\_ variant \_ t** set to the special value, DISP \_ E \_ PARAMNOTFOUND, and type, VT \_ ERROR. Alternativ können Sie **vtMissing** angeben, bei dem es sich um eine entsprechende vordefinierte Konstante handelt, die von der **\# Importdirektive** bereitgestellt wird.

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-oder verwenden –

```cpp 
 
...vtMissing...; 
```

### <a name="declaring-a-variant"></a>Deklarieren einer Variante

In Visual Basic wird ein **Variant** -Wert wie folgt mit der **Dim** -Anweisung deklariert:

```vb 
 
Dim VariableName As Variant 
```

Deklarieren Sie in Visual C++ eine Variable als **\_ Typvariante \_ t.** Nachfolgend sind einige schematische **\_ Variant t-Deklarationen \_** dargestellt.

> [!NOTE]
> [!HINWEIS] Diese Deklarationen geben Ihnen lediglich eine ungefähre Vorstellung davon, was Sie in Ihrem eigenen Programm codieren können. Weitere Informationen finden Sie in den Beispielen unten und in der Visual C++-Dokumentation.

```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

### <a name="using-arrays-of-variants"></a>Verwenden von Arrays von Varianten

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

Im folgenden Visual C++-Beispiel wird die Verwendung eines **SafeArray-Objekts veranschaulicht, das** mit einer **\_ Variante \_ t** verwendet wird.

> [!NOTE]
> [!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.

1. Once again, the TESTHR() inline function is defined to take advantage of the existing error-handling mechanism.

2. Sie benötigen nur ein eindimensionales Array, sodass Sie **SafeArrayCreateVector** verwenden können, statt der allgemeinen **SAFEARRAYBOUND** -Deklaration und der **SafeArrayCreate** -Funktion. Der Code würde wie folgt aussehen, wenn **SafeArrayCreate** verwendet wird:
    
   ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
   ```

3. Das durch die aufgezählte Konstante **adSchemaColumns** identifizierte Schema ist vier Einschränkungsspalten zugeordnet: TABLE \_ CATALOG, TABLE \_ SCHEMA, TABLE \_ NAME und COLUMN \_ NAME. Therefore, an array of **Variant** values with four elements is created. Anschließend wird ein Einschränkungswert angegeben, der der dritten Spalte, TABLE \_ NAME, entspricht. The **Recordset** that is returned consists of several columns, a subset of which is the constraint columns. The values of the constraint columns for each returned row must be the same as the corresponding constraint values.

4. Wenn Sie mit **SafeArrays** vertraut sind, überrascht es Sie möglicherweise, dass **SafeArrayDestroy()** nicht vor dem Ende aufgerufen wird. Tatsächlich wird durch den Aufruf von **SafeArrayDestroy()** in diesem Fall eine Laufzeitausnahme verursacht. Der Grund dafür ist, dass der Destruktor für vtCriteria **VariantClear**() aufruft, wenn die **\_ Variante \_ t** den Bereich übergibt, wodurch **SafeArray** freigegeben wird. Das Aufrufen von **SafeArrayDestroy** ohne manuelles Löschen der **\_ Variante \_ t** würde dazu führen, dass der Destruktor versucht, einen ungültigen **SafeArray-Zeiger** zu löschen. Wenn **SafeArrayDestroy** aufgerufen wird, würde der Code wie folgt aussehen:
    
   ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
   ```
    
   Es ist jedoch viel einfacher, die **\_ Variante \_ nicht** das **SafeArray** verwalten zu lassen.


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

### <a name="using-property-getputputref"></a>Verwenden der Eigenschaft "Get/Put/PutRef"

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

In diesem Visual C++-Beispiel wird die **Get** / **Put** / **PutRef-Eigenschaft** veranschaulicht.

> [!NOTE]
> [!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.

1. In diesem Beispiel werden zwei Formen eines fehlenden Zeichenfolgenarguments verwendet: eine explizite Konstante, **strMissing** und eine Zeichenfolge, die der Compiler zum Erstellen einer temporären **\_ bstr \_ t** verwendet, die für den Bereich der **Open-Methode** vorhanden ist.

2. Es ist nicht erforderlich, den Operanden von rs- \> PutRefActiveConnection(cn) in (IDispatch) zu umwandeln, \* da der Operandtyp bereits (IDispatch) \* ist.
    
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

### <a name="using-getitemx-and-itemx"></a>Verwenden von GetItem(x) und Item \[ x\]

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
> [!HINWEIS] Der folgende Hinweis entspricht kommentierten Abschnitten im Codebeispiel.

1. Wenn mit **Item** auf die Auflistung zugegriffen wird, muss der Index **2** in **long** umgewandelt werden, damit ein geeigneter Konstruktor aufgerufen wird.
    
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

### <a name="casting-ado-object-pointers-with-idispatch-"></a>Umwandeln von ADO-Objektzeigern mit "(IDispatch \*)"

The following Visual C++ example demonstrates using (IDispatch \*) to cast ADO object pointers.

> [!NOTE]
> [!HINWEIS] Die folgenden Hinweise entsprechen kommentierten Abschnitten im Codebeispiel.

1. Specify an open **Connection** object in an explicitly coded **Variant**. Wandeln Sie ihn mit (IDispatch) \* um, damit der richtige Konstruktor aufgerufen wird. Legen Sie außerdem den zweiten **\_ Variant \_ t-Parameter** explizit auf den Standardwert **"true"** fest, sodass die Anzahl der Objektverweise korrekt ist, wenn der **Recordset::Open-Vorgang** beendet wird.

2. Der Ausdruck ( \_ bstr \_ t) ist keine Umwandlung, sondern ein **\_ Variant \_ t-Operator,** der eine **\_ bstr \_ t-Zeichenfolge** aus dem von **Value** zurückgegebenen **Variant** extrahiert. Der Ausdruck (Char \* ) ist keine Umwandlung, sondern ein **\_ bstr \_ t-Operator,** der einen Zeiger auf die gekapselte Zeichenfolge in einem **\_ bstr \_ t-Objekt** extrahiert. In diesem Codeabschnitt werden einige der nützlichen Verhaltensweisen von **\_ Operatoren \_** der Varianten t und **\_ bstr \_ t** veranschaulicht.
    
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

