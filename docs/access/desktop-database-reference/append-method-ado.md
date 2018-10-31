---
title: Append-Methode (ADO)
TOCTitle: Append Method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03d3b7ac215c8b5328148b33e2e966c4e574c98e
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864005"
---
# <a name="append-method-ado"></a>Append-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013



Ein Objekt wird einer Auflistung angefügt. Bei einer [Fields](fields-collection-ado.md)-Auflistung wird möglicherweise ein neues [Field](field-object-ado.md)-Objekt erstellt, bevor es der Auflistung angefügt wird.

## <a name="syntax"></a>Syntax

*Auflistung*. Fügen Sie *-Objekt*

*Felder*. *Name*, *Typ*, *DefinedSize*, *Attrib*, *FieldValue* Anfügen

## <a name="parameters"></a>Parameter

  - *collection*

  - Ein Collection-Objekt.

  - *fields*

  - Eine **Fields** -Auflistung.

  - *Objekt*

  - Eine Objektvariable, durch die das anzufügende Objekt dargestellt wird.

  - *Name*

  - Ein **String**-Wert, der den Namen des neuen **Field**-Objekts enthält und nicht mit dem Namen eines anderen Objekts in *fields* übereinstimmen darf.

  - *Type*

  - Ein [DataTypeEnum](datatypeenum.md)-Wert, dessen Standardwert **adEmpty** ist und durch den der Datentyp des neuen Felds angegeben wird. Die folgenden Datentypen werden von ADO nicht unterstützt und sollten beim Anfügen neuer Felder an ein **Recordset** nicht verwendet werden: **adIDispatch**, **adIUnknown**, **adVariant**.

  - *DefinedSize*

  - Optional. Ein Long-Wert, durch den die definierte Größe des neuen Felds in Zeichen oder Byte dargestellt wird. Der Standardwert für diesen Parameter wird von Type abgeleitet. Felder mit einem DefinedSize-Wert von mehr als 255 Bytes werden als Spalten mit variabler Länge behandelt. (Der Standardwert für DefinedSize ist nicht angegeben.)

  - *Attrib*

  - Optional. Ein [FieldAttributeEnum](fieldattributeenum.md)-Wert, dessen Standardwert **adFldDefault** ist und durch den Attribute für das neue Feld angegeben werden. Wenn dieser Wert nicht angegeben ist, enthält das Feld von *Type* abgeleitete Werte.

  - *FieldValue*

  - Optional. Ein **Variant** -Objekt, durch das der Wert für das neue Feld dargestellt wird. Wenn nichts angegeben ist, wird dem Feld ein Nullwert angefügt.

## <a name="remarks"></a>Hinweise

**Parameters-Auflistung**

Sie müssen die [Type](type-property-ado.md)-Eigenschaft eines [Parameter](parameter-object-ado.md)-Objekts festlegen, bevor Sie es der **Parameters** -Auflistung anfügen. Wenn Sie einen Datentyp mit variabler Länge auswählen, müssen Sie auch die [Size](size-property-ado.md)-Eigenschaft auf einen größeren Wert als Null festlegen.

Indem Sie Parameter selbst beschreiben, minimieren Sie Aufrufe an den Anbieter und verbessern folglich die Leistung beim Verwenden gespeicherter Prozeduren oder parametrisierter Abfragen. Sie müssen jedoch die Eigenschaften der zur aufzurufenden gespeicherten Prozedur oder parametrisierten Abfrage zugeordneten Parameter kennen.

Verwenden Sie die [CreateParameter](createparameter-method-ado.md)-Methode, um **Parameter** -Objekte mit den entsprechenden Eigenschafteneinstellungen zu erstellen, und verwenden Sie die **Append** -Methode, um diese der [Parameters](parameters-collection-ado.md)-Auflistung hinzuzufügen. Auf diese Weise können Sie Parameterwerte festlegen und zurückgeben, ohne den Anbieter für die Parameterinformationen aufrufen zu müssen. Wenn Sie für einen Anbieter schreiben, von dem keine Parameterinformationen bereitgestellt werden, müssen Sie mit dieser Methode die **Parameters** -Auflistung manuell auffüllen, um überhaupt Parameter verwenden zu können.

**Fields-Auflistung**

Der *FieldValue* -Parameter ist nur gültig, wenn ein **Field** -Objekt eines [Record](record-object-ado.md) -Objekts, um ein **Recordset** -Objekt nicht hinzufügen. Mit einem **Record** -Objekt können Sie gleichzeitig Felder anfügen und Werte bereitstellen. Bei einem **Recordset** -Objekt müssen Sie Felder erstellen, während das **Recordset** geschlossen ist, dann das **Recordset** öffnen und den Feldern Werte zuweisen.


> [!NOTE]
> Bei neuen **Field** -Objekten, die der **Fields**-Auflistung eines **Record**-Objekts angefügt wurden, muss die [Value](value-property-ado.md) -Eigenschaft festgelegt werden, bevor andere **Field** -Eigenschaften angegeben werden. Zuerst müssen ein angegebener Wert für die **Value** -Eigenschaft zugewiesen und die [Update](update-method-ado.md)-Methode für die **Fields** -Auflistung aufgerufen worden sein. Anschließend kann auf weitere Eigenschaften, wie z. B. [Type](type-property-ado.md) oder [Attributes](attributes-property-ado.md), zugegriffen werden.


**Field**-Objekte der folgenden Datentypen (**DataTypeEnum**) können nicht der **Fields**-Auflistung angefügt werden und verursachen das Auftreten eines Fehlers: **adArray**, **adChapter**, **adEmpty**, **adPropVariant** und **adUserDefined**. Außerdem werden die folgenden Datentypen von ADO nicht unterstützt: **adIDispatch**, **adIUnknown** und **adIVariant**. Für diese Typen tritt beim Anfügen kein Fehler auf, aber die Verwendung kann zu unvorhersehbaren Ergebnissen, wie z. B. Speicherverlusten, führen.

**Recordset**

Wenn Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft nicht festlegen, bevor Sie die **Append** -Methode aufrufen, wird **CursorLocation** automatisch auf **adUseClient** (einen [CursorLocationEnum](cursorlocationenum.md)-Wert) festgelegt, wenn die [Open](recordset-object-ado.md)-Methode des [Recordset](open-method-ado-recordset.md)-Objekts aufgerufen wird.

Ein Laufzeitfehler tritt auf, wenn die **Append** -Methode für die **Fields** -Auflistung eines geöffneten **Recordsets** oder für ein **Recordset**, für das die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft festgelegt wurde, aufgerufen wird. Sie können nur Felder zu einem **Recordset** hinzufügen, das nicht geöffnet ist und noch nicht mit einer Datenquelle verbunden wurde. Dies ist normalerweise der Fall, wenn ein **Recordset** -Objekt mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt oder einer Objektvariablen zugewiesen wird.

**Record**

Es tritt kein Laufzeitfehler auf, wenn die **Append** -Methode für die **Fields** -Auflistung eines geöffneten **Record** -Objekts aufgerufen wird. Das neue Feld wird der **Fields** -Auflistung des **Record** -Objekts hinzugefügt. Wenn das **Record** -Objekt von einem **Recordset** abgeleitet wurde, wird das neue Feld nicht in der **Fields** -Auflistung des **Recordset** -Objekts angezeigt.

Sie können ein nicht vorhandenes Feld erstellen und der **Fields** -Auflistung anfügen, indem Sie dem Feldobjekt einen Wert zuweisen, als sei es bereits in der Auflistung vorhanden. Durch die Zuweisung wird die automatische Erstellung und Anfügung des **Field** -Objekts ausgelöst, dann wird die Zuweisung abgeschlossen.

Rufen Sie nach dem Anfügen eines **Field** -Objekts an die **Fields** -Auflistung eines **Record** -Objekts die **Update** -Methode der **Fields** -Auflistung auf, um die Änderung zu speichern.

