---
title: Verwenden von Visual C++-Erweiterungen
TOCTitle: Using Visual C++ Extensions
ms:assetid: 0fb1014c-7ab6-6add-d09f-e5e48b2b32cb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248866(v=office.15)
ms:contentKeyID: 48543270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0076eae8a930688219da413a31d73a376bc53a39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475518"
---
# <a name="using-visual-c-extensions"></a><span data-ttu-id="9710c-102">Verwenden von Visual C++-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="9710c-102">Using Visual C++ Extensions</span></span>


<span data-ttu-id="9710c-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9710c-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="the-iadorecordbinding-interface"></a><span data-ttu-id="9710c-104">Die IADORecordBinding-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9710c-104">The IADORecordBinding Interface</span></span>

<span data-ttu-id="9710c-p101">Durch die Microsoft Visual C++-Erweiterungen für ADO werden Felder eines [Recordset](recordset-object-ado.md)-Objekts C/C++-Variablen zugeordnet bzw. an diese gebunden. Wenn die aktuelle Zeile des gebundenen **Recordset** -Objekts geändert wird, werden alle gebundenen Felder in **Recordset** in die C/C++-Variablen kopiert. Gegebenenfalls werden die kopierten Daten in den deklarierten Typ der C/C++-Variablen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9710c-p101">The Microsoft Visual C++ Extensions for ADO associate, or bind, fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. Whenever the current row of the bound **Recordset** changes, all the bound fields in the **Recordset** are copied to the C/C++ variables. If necessary, the copied data is converted to the declared data type of the C/C++ variable.</span></span>

<span data-ttu-id="9710c-p102">Durch die **BindToRecordset** -Methode der **IADORecordBinding** -Schnittstelle werden Felder an C/C++-Variablen gebunden. Durch die **AddNew** -Methode wird eine neue Zeile dem gebundenen **Recordset** hinzugefügt. Durch die **Update** -Methode werden Felder in neuen Zeilen des **Recordset** -Objekts mit dem Wert der C/C++-Variablen aufgefüllt oder Felder in vorhandenen Zeilen mit diesem Wert aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9710c-p102">The **BindToRecordset** method of the **IADORecordBinding** interface binds fields to C/C++ variables. The **AddNew** method adds a new row to the bound **Recordset**. The **Update** method populates fields in new rows of the **Recordset**, or updates fields in existing rows, with the value of the C/C++ variables.</span></span>

<span data-ttu-id="9710c-p103">Die **IADORecordBinding** -Schnittstelle wird durch das **Recordset** -Objekt implementiert. Sie müssen den Code für die Implementierung nicht selbst schreiben.</span><span class="sxs-lookup"><span data-stu-id="9710c-p103">The **IADORecordBinding** interface is implemented by the **Recordset** object. You do not code the implementation yourself.</span></span>

## <a name="binding-entries"></a><span data-ttu-id="9710c-113">Bindungseinträge</span><span class="sxs-lookup"><span data-stu-id="9710c-113">Binding Entries</span></span>

<span data-ttu-id="9710c-p104">Durch die Visual C++-Erweiterungen für ADO werden Felder eines [Recordset](recordset-object-ado.md)-Objekts C/C++-Variablen zugeordnet. Die Definition einer Zuordnung zwischen einem Feld und einer Variablen wird als *Bindungseintrag* bezeichnet. Bindungseinträge für numerische Daten und Daten mit fester und variabler Länge werden von Makros bereitgestellt. Die Bindungseinträge und C/C++-Variablen werden in **CADORecordBinding**, einer von der Visual C++-Erweiterungsklasse abgeleiteten Klasse, deklariert. Die **CADORecordBinding**-Klasse wird intern durch die Bindungseintragsmakros definiert.</span><span class="sxs-lookup"><span data-stu-id="9710c-p104">The Visual C++ Extensions for ADO map fields of a [Recordset](recordset-object-ado.md) object to C/C++ variables. The definition of a mapping between a field and a variable is called a *binding entry*. Macros provide binding entries for numeric, fixed-length, and variable-length data. The binding entries and C/C++ variables are declared in a class derived from the Visual C++ Extensions class, **CADORecordBinding**. The **CADORecordBinding** class is defined internally by the binding entry macros.</span></span>

<span data-ttu-id="9710c-p105">Die Parameter in diesen Makros werden von ADO intern einer **DBBINDING**-OLE DB-Struktur zugeordnet, und es wird ein **Accessor**-OLE DB-Objekt zum Verwalten der Verschiebung und Konvertierung von Daten zwischen Feldern und Variablen erstellt. Durch OLE DB werden Daten als aus drei Teilen bestehend definiert: ein *Puffer*, in dem die Daten gespeichert werden; ein *Status*, durch den angegeben wird, ob ein Feld erfolgreich im Puffer gespeichert wurde oder wie die Variable im Feld wiederhergestellt werden soll, und die *Länge* der Daten. (Weitere Informationen finden Sie unter *OLE DB-Programmierreferenz*, "Kapitel 6: Abrufen und Festlegen von Daten".)</span><span class="sxs-lookup"><span data-stu-id="9710c-p105">ADO internally maps the parameters in these macros to an OLE DB **DBBINDING** structure and creates an OLE DB **Accessor** object to manage the movement and conversion of data between fields and variables. OLE DB defines data as consisting of three parts: A *buffer* where the data is stored; a *status* that indicates whether a field was successfully stored in the buffer, or how the variable should be restored to the field; and the *length* of the data. (See the *OLE DB Programmer's Reference*, Chapter 6: Getting and Setting Data for more information.)</span></span>

## <a name="header-file"></a><span data-ttu-id="9710c-122">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="9710c-122">Header File</span></span>

<span data-ttu-id="9710c-123">Schließen Sie die folgende Datei in die Anwendung ein, um die Visual C++-Erweiterungen für ADO zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="9710c-123">Include the following file in your application in order to use the Visual C++ Extensions for ADO:</span></span>

```cpp 
 
#include <icrsint.h> 
```

## <a name="binding-recordset-fields"></a><span data-ttu-id="9710c-124">Binden von Recordset-Feldern</span><span class="sxs-lookup"><span data-stu-id="9710c-124">Binding Recordset Fields</span></span>

<span data-ttu-id="9710c-125">\*\*So binden Sie **Recordset** -Felder an C/C++-Variablen \*\*</span><span class="sxs-lookup"><span data-stu-id="9710c-125">**To Bind Recordset Fields to C/C++ Variables**</span></span>

1.  <span data-ttu-id="9710c-126">Erstellen Sie eine Klasse, die von der **CADORecordBinding** -Klasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9710c-126">Create a class derived from the **CADORecordBinding** class.</span></span>

2.  <span data-ttu-id="9710c-127">Geben Sie Bindungseinträge und entsprechende C/C++-Variablen in der abgeleiteten Klasse an.</span><span class="sxs-lookup"><span data-stu-id="9710c-127">Specify binding entries and corresponding C/C++ variables in the derived class.</span></span> <span data-ttu-id="9710c-128">Die Bindungseinträge zwischen **beginnen\_ADO\_BINDUNG** und **END\_ADO\_BINDUNG** Makros.</span><span class="sxs-lookup"><span data-stu-id="9710c-128">Bracket the binding entries between **BEGIN\_ADO\_BINDING** and **END\_ADO\_BINDING** macros.</span></span> <span data-ttu-id="9710c-129">Beenden Sie die Makros nicht mit Kommas oder Semikolons.</span><span class="sxs-lookup"><span data-stu-id="9710c-129">Do not terminate the macros with commas or semicolons.</span></span> <span data-ttu-id="9710c-130">Die entsprechenden Trennzeichen werden automatisch durch die einzelnen Makros angegeben.</span><span class="sxs-lookup"><span data-stu-id="9710c-130">Appropriate delimiters are specified automatically by each macro.</span></span> <span data-ttu-id="9710c-131">Geben Sie einen Bindungseintrag für jedes Feld an, das einer C/C++-Variablen zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9710c-131">Specify one binding entry for each field to be mapped to a C/C++ variable.</span></span> <span data-ttu-id="9710c-132">Verwenden Sie einen entsprechenden Member aus der **ADO\_FIXED\_Länge\_Eintrag**, **ADO\_numerischen\_Eintrag**, oder **ADO\_VARIABLE\_Länge\_Eintrag** Produktfamilie von Makros.</span><span class="sxs-lookup"><span data-stu-id="9710c-132">Use an appropriate member from the **ADO\_FIXED\_LENGTH\_ENTRY**, **ADO\_NUMERIC\_ENTRY**, or **ADO\_VARIABLE\_LENGTH\_ENTRY** family of macros.</span></span>

3.  <span data-ttu-id="9710c-p107">Erstellen Sie in der Anwendung eine Instanz der von **CADORecordBinding** abgeleiteten Klasse. Rufen Sie die **IADORecordBinding** -Schnittstelle aus dem **Recordset** -Objekt ab. Rufen Sie dann die **BindToRecordset** -Methode auf, um die **Recordset** -Felder an die C/C++-Variablen zu binden.</span><span class="sxs-lookup"><span data-stu-id="9710c-p107">In your application, create an instance of the class derived from **CADORecordBinding**. Get the **IADORecordBinding** interface from the **Recordset**. Then call the **BindToRecordset** method to bind the **Recordset** fields to the C/C++ variables.</span></span>

<span data-ttu-id="9710c-136">Weitere Informationen finden Sie unter [Visual C++-Erweiterungen (Beispiel)](visual-c-extensions-example.md).</span><span class="sxs-lookup"><span data-stu-id="9710c-136">See the [Visual C++ Extensions Example](visual-c-extensions-example.md) for more information.</span></span>

## <a name="interface-methods"></a><span data-ttu-id="9710c-137">Schnittstellenmethoden</span><span class="sxs-lookup"><span data-stu-id="9710c-137">Interface Methods</span></span>

<span data-ttu-id="9710c-p108">Die **IADORecordBinding** -Schnittstelle verfügt über drei Methoden: **BindToRecordset**, **AddNew** und **Update**. Das einzige Argument für jede Methode ist ein Zeiger auf eine Instanz der von **CADORecordBinding** abgeleiteten Klasse. Daher können mit den Methoden **AddNew** und **Update** keine Parameter der ADO-Methoden gleichen Namens angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9710c-p108">The **IADORecordBinding** interface has three methods: **BindToRecordset**, **AddNew**, and **Update**. The sole argument to each method is a pointer to an instance of the class derived from **CADORecordBinding**. Therefore, the **AddNew** and **Update** methods cannot specify any of the parameters of their ADO method namesakes.</span></span>

<span data-ttu-id="9710c-141">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9710c-141">**Syntax**</span></span>

<span data-ttu-id="9710c-142">Durch die **BindToRecordset** -Methode werden die **Recordset** -Felder C/C++-Variablen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9710c-142">The **BindToRecordset** method associates the **Recordset** fields with C/C++ variables.</span></span>

`BindToRecordset(CADORecordBinding *binding)` 

<span data-ttu-id="9710c-143">Durch die **AddNew** -Methode wird die gleichnamige ADO-Methode, [AddNew](addnew-method-ado.md), aufgerufen, um dem **Recordset** -Objekt eine neue Zeile hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9710c-143">The **AddNew** method invokes its namesake, the ADO [AddNew](addnew-method-ado.md) method, to add a new row to the **Recordset**.</span></span>

`AddNew(CADORecordBinding *binding)` 

<span data-ttu-id="9710c-144">Durch die **Update** -Methode wird die gleichnamige ADO-Methode, [Update](update-method-ado.md), aufgerufen, um das **Recordset** -Objekt zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9710c-144">The **Update** method invokes its namesake, the ADO [Update](update-method-ado.md) method, to update the **Recordset**.</span></span>

`Update(CADORecordBinding *binding)` 

## <a name="binding-entry-macros"></a><span data-ttu-id="9710c-145">Bindungseintragsmakros</span><span class="sxs-lookup"><span data-stu-id="9710c-145">Binding Entry Macros</span></span>

<span data-ttu-id="9710c-p109">Durch Bindungseintragsmakros wird die Zuordnung eines **Recordset** -Felds und einer Variablen definiert. Der Satz Bindungseinträge wird durch ein Anfangs- und ein Endmakro begrenzt.</span><span class="sxs-lookup"><span data-stu-id="9710c-p109">Binding entry macros define the association of a **Recordset** field and a variable. A beginning and ending macro delimits the set of binding entries.</span></span>

<span data-ttu-id="9710c-p110">Für Daten mit fester Länge (z. B. **adDate** oder **adBoolean** ), numerische Daten (z. B. **adTinyInt**, **adInteger** oder **adDouble** ) und Daten mit variabler Länge (z. B. **adChar**, **adVarChar** oder **adVarBinary** ) werden Makrofamilien bereitgestellt. Alle numerischen Typen, mit Ausnahme von **adVarNumeric**, sind auch Typen mit fester Länge. Jede Familie enthält unterschiedliche Parametersätze, sodass Sie Bindungsinformationen, die nicht von Interesse sind, ausschließen können.</span><span class="sxs-lookup"><span data-stu-id="9710c-p110">Families of macros are provided for fixed-length data, such as **adDate** or **adBoolean**; numeric data, such as **adTinyInt**, **adInteger**, or **adDouble**; and variable-length data, such as **adChar**, **adVarChar** or **adVarBinary**. All numeric types, except for **adVarNumeric**, are also fixed-length types. Each family has differing sets of parameters so that you can exclude binding information that is of no interest.</span></span>

<span data-ttu-id="9710c-151">Finden Sie unter *OLE DB Programmer's Reference* Anhang A: Datentypen für zusätzliche Informationen.</span><span class="sxs-lookup"><span data-stu-id="9710c-151">See the *OLE DB Programmer's Reference,* Appendix A: Data Types for additional information.</span></span>

<span data-ttu-id="9710c-152">_**Bindungsanfangseinträge**_</span><span class="sxs-lookup"><span data-stu-id="9710c-152">_**Begin Binding Entries**_</span></span>

<span data-ttu-id="9710c-153">**BEGINNEN\_ADO\_binden**(*Klasse*)</span><span class="sxs-lookup"><span data-stu-id="9710c-153">**BEGIN\_ADO\_BINDING**(*Class*)</span></span>

<span data-ttu-id="9710c-154">_**Daten mit variabler Länge**_</span><span class="sxs-lookup"><span data-stu-id="9710c-154">_**Fixed-Length Data**_</span></span>

<span data-ttu-id="9710c-155">**ADO\_FIXED\_Länge\_Eintrag**(*Ordnungszahl, Datentyp, Puffer Status, ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-155">**ADO\_FIXED\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Status, Modify*)</span></span>  
<span data-ttu-id="9710c-156">**ADO\_FIXED\_Länge\_ENTRY2**(*Ordnungszahl, Datentyp, Puffer ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-156">**ADO\_FIXED\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Modify*)</span></span>

<span data-ttu-id="9710c-157">_**Numerische Daten**_</span><span class="sxs-lookup"><span data-stu-id="9710c-157">_**Numeric Data**_</span></span>

<span data-ttu-id="9710c-158">**ADO\_numerischen\_Eintrag**(*Ordnungszahl, Datentyp, Puffer, Genauigkeit, Skalierung, Status, ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-158">**ADO\_NUMERIC\_ENTRY**(*Ordinal, DataType, Buffer, Precision, Scale, Status, Modify*)</span></span>  
<span data-ttu-id="9710c-159">**ADO\_numerischen\_ENTRY2**(*Ordnungszahl, Datentyp, Puffer, Genauigkeit, Skalierung ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-159">**ADO\_NUMERIC\_ENTRY2**(*Ordinal, DataType, Buffer, Precision, Scale, Modify*)</span></span>

<span data-ttu-id="9710c-160">_**Daten mit variabler Länge**_</span><span class="sxs-lookup"><span data-stu-id="9710c-160">_**Variable-Length Data**_</span></span>

<span data-ttu-id="9710c-161">**ADO\_VARIABLE\_Länge\_Eintrag**(*Ordnungszahl, Datentyp, Puffer, Größe, Status, Länge ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-161">**ADO\_VARIABLE\_LENGTH\_ENTRY**(*Ordinal, DataType, Buffer, Size, Status, Length, Modify*)</span></span>  
<span data-ttu-id="9710c-162">**ADO\_VARIABLE\_Länge\_ENTRY2**(*Ordnungszahl, Datentyp, Puffer, Größe, Status, ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-162">**ADO\_VARIABLE\_LENGTH\_ENTRY2**(*Ordinal, DataType, Buffer, Size, Status, Modify*)</span></span>  
<span data-ttu-id="9710c-163">**ADO\_VARIABLE\_Länge\_ENTRY3**(*Ordnungszahl, Datentyp, Puffer, Größe, Länge, ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-163">**ADO\_VARIABLE\_LENGTH\_ENTRY3**(*Ordinal, DataType, Buffer, Size, Length, Modify*)</span></span>  
<span data-ttu-id="9710c-164">**ADO\_VARIABLE\_Länge\_ENTRY4**(*Ordnungszahl, Datentyp, Puffer, Größe ändern*)</span><span class="sxs-lookup"><span data-stu-id="9710c-164">**ADO\_VARIABLE\_LENGTH\_ENTRY4**(*Ordinal, DataType, Buffer, Size, Modify*)</span></span>

<span data-ttu-id="9710c-165">_**Bindungsendeinträge**_</span><span class="sxs-lookup"><span data-stu-id="9710c-165">_**End Binding Entries**_</span></span>

<span data-ttu-id="9710c-166">**END\_ADO\_binden** ()</span><span class="sxs-lookup"><span data-stu-id="9710c-166">**END\_ADO\_BINDING**()</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9710c-167">Parameter</span><span class="sxs-lookup"><span data-stu-id="9710c-167">Parameter</span></span></p></th>
<th><p><span data-ttu-id="9710c-168">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9710c-168">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9710c-169"><em>Class</em></span><span class="sxs-lookup"><span data-stu-id="9710c-169"><em>Class</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-170">Klasse, in der die Bindungseinträge und C/C++-Variablen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9710c-170">Class in which the binding entries and C/C++ variables are defined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-171"><em>Ordinal</em></span><span class="sxs-lookup"><span data-stu-id="9710c-171"><em>Ordinal</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-172">Ab Eins gezählte Ordnungszahl des <strong>Recordset</strong>-Felds, das der C/C++-Variablen entspricht.</span><span class="sxs-lookup"><span data-stu-id="9710c-172">Ordinal number, counting from one, of the <strong>Recordset</strong> field corresponding to your C/C++ variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-173"><em>DataType</em></span><span class="sxs-lookup"><span data-stu-id="9710c-173"><em>DataType</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-p111">Entsprechender ADO-Datentyp der C/C++-Variablen (eine Liste der gültigen Datentypen finden Sie unter <a href="datatypeenum.md">DataTypeEnum</a>). Der Wert des <strong>Recordset</strong>-Felds wird gegebenenfalls in diesen Datentyp konvertiert.</span><span class="sxs-lookup"><span data-stu-id="9710c-p111">Equivalent ADO data type of the C/C++ variable (see <a href="datatypeenum.md">DataTypeEnum</a> for a list of valid data types). The value of the <strong>Recordset</strong> field will be converted to this data type if necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-176"><em>Buffer</em></span><span class="sxs-lookup"><span data-stu-id="9710c-176"><em>Buffer</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-177">Name der C/C++-Variablen, in der das <strong>Recordset</strong>-Feld gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9710c-177">Name of the C/C++ variable where the <strong>Recordset</strong> field will be stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-178"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="9710c-178"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-p112">Maximale Größe von <em>Buffer</em> in Byte. Wenn <em>Buffer</em> eine Zeichenfolge mit variabler Länge enthält, lassen Sie Platz für eine Null am Ende.</span><span class="sxs-lookup"><span data-stu-id="9710c-p112">Maximum size in bytes of <em>Buffer</em>. If <em>Buffer</em> will contain a variable-length string, allow room for a terminating zero.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-181"><em>Status</em></span><span class="sxs-lookup"><span data-stu-id="9710c-181"><em>Status</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-182">Name einer Variablen, durch die angegeben wird, ob der Inhalt von <em>Buffer</em> gültig ist und ob die Konvertierung des Felds in <em>DataType</em> erfolgreich war.
</span><span class="sxs-lookup"><span data-stu-id="9710c-182">Name of a variable that will indicate whether the contents of <em>Buffer</em> are valid, and whether the conversion of the field to <em>DataType</em> was successful.</span></span> <span data-ttu-id="9710c-183">Die beiden wichtigsten Werte für diese Variable sind <strong>adFldOK</strong> (die Konvertierung war erfolgreich) und <strong>adFldNull</strong> (der Wert des Felds wäre ein VARIANT vom Typ VT_NULL und nicht lediglich leer).</span><span class="sxs-lookup"><span data-stu-id="9710c-183">The two most important values for this variable are <strong>adFldOK</strong>, which means the conversion was successful; and <strong>adFldNull</strong>, which means the value of the field would be a VARIANT of type VT_NULL and not merely empty.</span></span> <span data-ttu-id="9710c-184">Mögliche Werte für <em>Status</em> in der folgenden Tabelle aufgelisteten &quot;Statuswerte.&quot;</span><span class="sxs-lookup"><span data-stu-id="9710c-184">Possible values for <em>Status</em> are listed in the next table, &quot;Status Values.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-185"><em>Modify</em></span><span class="sxs-lookup"><span data-stu-id="9710c-185"><em>Modify</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-186">Boolesches Flag; durch TRUE wird angegeben, dass ADO das entsprechende <strong>Recordset</strong>-Feld mit dem in <em>Buffer</em> enthaltenen Wert aktualisieren darf.
</span><span class="sxs-lookup"><span data-stu-id="9710c-186">Boolean flag; if TRUE, indicates ADO is allowed to update the corresponding <strong>Recordset</strong> field with the value contained in <em>Buffer</em>.</span></span> <span data-ttu-id="9710c-187">Legen Sie den booleschen <em>modify</em>-Parameter auf TRUE fest, um zu ermöglichen, dass das gebundene Feld durch ADO aktualisiert wird. Legen Sie ihn auf FALSE fest, wenn Sie das Feld untersuchen möchten, ohne es zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9710c-187">Set the Boolean <em>modify</em> parameter to TRUE to enable ADO to update the bound field, and FALSE if you want to examine the field but not change it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-188"><em>Precision</em></span><span class="sxs-lookup"><span data-stu-id="9710c-188"><em>Precision</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-189">Anzahl der Ziffern, die in einer numerischen Variablen dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="9710c-189">Number of digits that can be represented in a numeric variable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-190"><em>Scale</em></span><span class="sxs-lookup"><span data-stu-id="9710c-190"><em>Scale</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-191">Anzahl der Dezimalstellen in einer numerischen Variablen.</span><span class="sxs-lookup"><span data-stu-id="9710c-191">Number of decimal places in a numeric variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-192"><em>Length</em></span><span class="sxs-lookup"><span data-stu-id="9710c-192"><em>Length</em></span></span></p></td>
<td><p><span data-ttu-id="9710c-193">Name einer 4-Byte-Variablen, die die tatsächliche Länge der Daten in <em>Buffer</em> enthält.</span><span class="sxs-lookup"><span data-stu-id="9710c-193">Name of a four-byte variable that will contain the actual length of the data in <em>Buffer</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="status-values"></a><span data-ttu-id="9710c-194">Statuswerte</span><span class="sxs-lookup"><span data-stu-id="9710c-194">Status Values</span></span>

<span data-ttu-id="9710c-195">Der Wert der Variablen *Status* gibt an, ob ein Feld erfolgreich in eine Variable kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9710c-195">The value of the *Status* variable indicates whether a field was successfully copied to a variable.</span></span>

<span data-ttu-id="9710c-196">Beim Festlegen von Daten kann *Status* auf **adFldNull** festgelegt werden, um anzugeben, dass das **Recordset**-Feld auf Null festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9710c-196">When setting data, *Status* may be set to **adFldNull** to indicate the **Recordset** field should be set to null.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9710c-197">Konstante</span><span class="sxs-lookup"><span data-stu-id="9710c-197">Constant</span></span></p></th>
<th><p><span data-ttu-id="9710c-198">Wert</span><span class="sxs-lookup"><span data-stu-id="9710c-198">Value</span></span></p></th>
<th><p><span data-ttu-id="9710c-199">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9710c-199">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9710c-200"><strong>adFldOK</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-200"><strong>adFldOK</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-201">0</span><span class="sxs-lookup"><span data-stu-id="9710c-201">0</span></span></p></td>
<td><p><span data-ttu-id="9710c-202">Ein Feldwert ungleich Null wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9710c-202">A non-null field value was returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-203"><strong>adFldBadAccessor</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-203"><strong>adFldBadAccessor</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-204">1</span><span class="sxs-lookup"><span data-stu-id="9710c-204">1</span></span></p></td>
<td><p><span data-ttu-id="9710c-205">Bindung war ungültig.</span><span class="sxs-lookup"><span data-stu-id="9710c-205">Binding was invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-206"><strong>adFldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-206"><strong>adFldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-207">2</span><span class="sxs-lookup"><span data-stu-id="9710c-207">2</span></span></p></td>
<td><p><span data-ttu-id="9710c-208">Wert konnte aus anderen Gründen als nicht übereinstimmenden Vorzeichen oder einem Datenüberlauf nicht konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="9710c-208">Value couldn't be converted for reasons other than sign mismatch or data overflow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-209"><strong>adFldNull</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-209"><strong>adFldNull</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-210">3</span><span class="sxs-lookup"><span data-stu-id="9710c-210">3</span></span></p></td>
<td><p><span data-ttu-id="9710c-211">Beim Abrufen eines Felds wird angegeben, dass ein Nullwert zurückgegeben wurde.
</span><span class="sxs-lookup"><span data-stu-id="9710c-211">When getting a field, indicates a null value was returned.</span></span> <span data-ttu-id="9710c-212">Beim Festlegen eines Felds wird angegeben, dass das Feld auf <strong>NULL</strong> festgelegt werden soll, wenn <strong>NULL</strong> selbst vom Feld nicht codiert werden kann (z. B. ein Zeichenarray oder eine Ganzzahl).</span><span class="sxs-lookup"><span data-stu-id="9710c-212">When setting a field, indicates the field should be set to <strong>NULL</strong> when the field cannot encode <strong>NULL</strong> itself (for example, a character array or an integer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-213"><strong>adFldTruncated</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-213"><strong>adFldTruncated</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-214">4</span><span class="sxs-lookup"><span data-stu-id="9710c-214">4</span></span></p></td>
<td><p><span data-ttu-id="9710c-215">Daten mit variabler Länge oder numerische Ziffern wurden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="9710c-215">Variable-length data or numeric digits were truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-216"><strong>adFldSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-216"><strong>adFldSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-217">5</span><span class="sxs-lookup"><span data-stu-id="9710c-217">5</span></span></p></td>
<td><p><span data-ttu-id="9710c-218">Wert ist signiert und variabler Datentyp ist nicht signiert.</span><span class="sxs-lookup"><span data-stu-id="9710c-218">Value is signed and variable data type is unsigned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-219"><strong>adFldDataOverFlow</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-219"><strong>adFldDataOverFlow</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-220">6</span><span class="sxs-lookup"><span data-stu-id="9710c-220">6</span></span></p></td>
<td><p><span data-ttu-id="9710c-221">Wert ist zu groß zum Speichern im variablen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="9710c-221">Value is larger than could be stored in the variable data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-222"><strong>adFldCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-222"><strong>adFldCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-223">7</span><span class="sxs-lookup"><span data-stu-id="9710c-223">7</span></span></p></td>
<td><p><span data-ttu-id="9710c-224">Unbekannter Spaltentyp und Feld bereits geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9710c-224">Unknown column type and field already open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-225"><strong>adFldUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-225"><strong>adFldUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-226">8</span><span class="sxs-lookup"><span data-stu-id="9710c-226">8</span></span></p></td>
<td><p><span data-ttu-id="9710c-227">Feldwert konnte nicht ermittelt werden - z. B. in einem neuen nicht zugewiesenen Feld ohne Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9710c-227">Field value could not be determined — for example, on a new, unassigned field with no default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-228"><strong>adFldPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-228"><strong>adFldPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-229">9</span><span class="sxs-lookup"><span data-stu-id="9710c-229">9</span></span></p></td>
<td><p><span data-ttu-id="9710c-230">Beim Aktualisieren keine Berechtigung zum Schreiben von Daten.</span><span class="sxs-lookup"><span data-stu-id="9710c-230">When updating, no permission to write data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-231"><strong>adFldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-231"><strong>adFldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-232">10</span><span class="sxs-lookup"><span data-stu-id="9710c-232">10</span></span></p></td>
<td><p><span data-ttu-id="9710c-233">Beim Aktualisieren würde durch den Feldwert die Spaltenintegrität verletzt werden.</span><span class="sxs-lookup"><span data-stu-id="9710c-233">When updating, field value would violate column integrity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-234"><strong>adFldSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-234"><strong>adFldSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-235">11</span><span class="sxs-lookup"><span data-stu-id="9710c-235">11</span></span></p></td>
<td><p><span data-ttu-id="9710c-236">Beim Aktualisieren würde durch den Feldwert das Spaltenschema verletzt werden.</span><span class="sxs-lookup"><span data-stu-id="9710c-236">When updating, field value would violate column schema.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9710c-237"><strong>adFldBadStatus</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-237"><strong>adFldBadStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-238">12</span><span class="sxs-lookup"><span data-stu-id="9710c-238">12</span></span></p></td>
<td><p><span data-ttu-id="9710c-239">Beim Aktualisieren ungültiger Statusparameter.</span><span class="sxs-lookup"><span data-stu-id="9710c-239">When updating, invalid status parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9710c-240"><strong>adFldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="9710c-240"><strong>adFldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="9710c-241">13</span><span class="sxs-lookup"><span data-stu-id="9710c-241">13</span></span></p></td>
<td><p><span data-ttu-id="9710c-242">Beim Aktualisieren wurde ein Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="9710c-242">When updating, a default value was used.</span></span></p></td>
</tr>
</tbody>
</table>

