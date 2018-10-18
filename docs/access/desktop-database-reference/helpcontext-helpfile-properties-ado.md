---
<<<<<<< HEAD-Titel: HelpContext- und HelpFile-Eigenschaften (ADO) TOCTitle: HelpContext-und HelpFile-Eigenschaften (ADO) Ms:assetid: 8a79f994-f17c-2983-0593-095801be762e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) Ms:contentKeyID: 48546194 ms.date: 09/18 / 2015 Mtps_version: Office. 15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext- und HelpFile-Eigenschaft (ADO)

=== Titel: HelpContext-und HelpFile-Eigenschaft (ADO) TOCTitle: HelpContext-und HelpFile-Eigenschaft (ADO) Ms:assetid: 8a79f994-f17c-2983-0593-095801be762e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) Ms:contentKeyID: 48546194 ms.date: 10/17/2018 Mtps_version: Office. 15
---

# <a name="helpcontext-helpfile-properties-ado"></a>HelpContext-und HelpFile-Eigenschaft (ADO)
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

Gibt die Hilfedatei und das Hilfethema an, das einem [Error](error-object-ado.md)-Objekt zugeordnet ist.

<<<<<<< Kopf
## <a name="return-values"></a>Rückgabewerte

  - **HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.

  - **HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.
=======
## <a name="return-values"></a>Rückgabewerte

- **HelpContextID** - gibt eine Kontext-ID als **Long** -Wert für ein Thema in einer Hilfedatei zurück.

- **HelpFile** - gibt einen **String** -Wert zurück, der als vollständig aufgelöster Pfad zu einer Hilfedatei ausgewertet wird.
>>>>>>> master

## <a name="remarks"></a>Hinweise

Wenn in der **HelpFile** -Eigenschaft eine Hilfedatei angegeben ist, wird mit der **HelpContext** -Eigenschaft automatisch das darin identifizierte Hilfethema angezeigt. Ist kein relevantes Hilfethema verfügbar, gibt die **HelpContext** -Eigenschaft Null zurück, und die **HelpFile** -Eigenschaft gibt eine leere Zeichenfolge ("") zurück.

