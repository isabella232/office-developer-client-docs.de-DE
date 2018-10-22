---
<<<<<<< HEAD-Titel: ParentURL-Eigenschaft (ADO) TOCTitle: ParentURL-Eigenschaft (ADO) === Titel: ParentURL-Eigenschaft (ADO) TOCTitle: ParentURL-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) Ms:contentKeyID: 48548517 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="parenturl-property-ado"></a>ParentURL-Eigenschaft (ADO)
=======
# <a name="parenturl-property-ado"></a>ParentURL-Eigenschaft (ADO)
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

Gibt die Zeichenfolge einer absoluten URL an, die auf das übergeordnete [Record](record-object-ado.md)-Objekt des aktuellen **Record** -Objekts verweist.

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen **String** -Wert zurück, der die URL des übergeordneten **Record** -Objekts angibt.

## <a name="remarks"></a>Hinweise

Die **ParentURL** -Eigenschaft hängt von der Quelle ab, die zum Öffnen des **Record** -Objekts verwendet wird. Das **Record** -Objekt kann beispielsweise mit einer Quelle geöffnet werden, die einen relativen Pfadnamen eines Verzeichnisses enthält, auf das von der [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft verwiesen wird.

Angenommen, "second" ist ein Ordner, der unter "first" enthalten ist. Öffnen Sie das **Record** -Objekt folgendermaßen:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Nun, der Wert der **ParentURL** -Eigenschaft ist **ParentURL** -Eigenschaft ist "https://first", genau wie **ActiveConnection**.

Die Quelle kann auch eine absolute URL sein, wie z. B. "https://first/second". **ParentURL** -Eigenschaft ist "https://first", die Ebene über. **ParentURL** -Eigenschaft ist "https://first", die Ebene über "Sekunde".

Diese Eigenschaft kann in den folgenden Fällen ein Nullwert sein:

- Für das aktuelle Objekt gibt es kein übergeordnetes Objekt. Beispiel: Wenn das **Record** -Objekt den Stamm eines Verzeichnisses darstellt.

- Das **Record** -Objekt stellt eine Entität dar, die mit einer URL nicht angegeben werden kann.

Die Eigenschaft ist schreibgeschützt.


> [!NOTE]
> - [!HINWEIS] Diese Eigenschaft wird nur von Dokumentquellenanbietern wie z. B. [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) unterstützt. Weitere Informationen finden Sie unter [Datensätze und vom Anbieter bereitgestellte Felder](records-and-provider-supplied-fields.md).
> - [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der Microsoft OLE DB Provider für Internet Publishing automatisch aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md). 
> - [!HINWEIS] Enthält der aktuelle Datensatz einen Datensatz aus einem ADO- **Recordset** -Objekt, verursacht der Zugriff auf die **ParentURL** -Eigenschaft einen Laufzeitfehler, der angibt, dass keine URL möglich ist.

