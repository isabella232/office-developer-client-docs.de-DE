---
title: ActiveConnection-Eigenschaft (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 372dac11500647af75881ae6b4aee22a391a32c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280529"
---
# <a name="activeconnection-property-ado-md"></a>ActiveConnection-Eigenschaft (ADO MD)

**Gilt für**: Access 2013, Office 2013

Gibt an, zu welchem ADO-[Connection](connection-object-ado.md)-Objekt die aktuelle Zellmenge oder der Katalog momentan gehört.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Variant**-Wert fest oder gibt diesen zurück. Der Wert enthält eine Zeichenfolge, die eine Verbindung oder ein **Connection**-Objekt definiert. Die Standardeinstellung ist eine leere Zeichenfolge.

## <a name="remarks"></a>Bemerkungen

Sie können diese Eigenschaft auf ein gültiges ADO- **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festlegen. Wenn diese Eigenschaft auf eine Verbindungszeichenfolge festgelegt wird, erstellt der Anbieter mithilfe dieser Definition ein neues **Connection** -Objekt und öffnet die Verbindung.

Wenn Sie das **ActiveConnection** -Argument der [Open](open-method-ado-md.md)-Methode verwenden, um ein [Cellset](cellset-object-ado-md.md)-Objekt zu öffnen, erbt die **ActiveConnection** -Eigenschaft den Wert des Arguments.

Beim Festlegen der **ActiveConnection** -Eigenschaft eines [Catalog](catalog-object-ado-md.md)-Objekts auf **Nothing** werden die verbundenen Daten freigegeben, einschließlich der Daten in der [CubeDefs](cubedefs-collection-ado-md.md)-Auflistung und der verbundenen [Dimension](dimension-object-ado-md.md)-, [Hierarchy](hierarchy-object-ado-md.md)-, [Level](level-object-ado-md.md)- und [Member](member-object-ado-md.md)-Objekte. Beim Schließen eines **Connection** -Objekts, das verwendet wurde, um ein **Catalog** -Objekt zu öffnen, wird dieselbe Wirkung wie beim Festlegen der **ActiveConnection** -Eigenschaft auf **Nothing** erzielt.

Durch Ändern der Standarddatenbank der Verbindung, auf die durch die **ActiveConnection** -Eigenschaft eines **Catalog** -Objekts verwiesen wurde, wird der Inhalt des **Catalog** -Objekts ungültig.

Wenn Sie versuchen, die **ActiveConnection** -Eigenschaft für ein geöffnetes **Cellset** -Objekt zu ändern, tritt ein Fehler auf.

> [!NOTE]
> [!HINWEIS] Achten Sie in Visual Basic darauf, das **Set** -Schlüsselwort zu verwenden, wenn Sie die **ActiveConnection** -Eigenschaft auf ein **Connection** -Objekt festlegen. Wenn Sie das **Set** -Schlüsselwort nicht verwenden, legen Sie die **ActiveConnection** -Eigenschaft gleich der Standardeigenschaft des **Connection** -Objekts , **ConnectionString**, fest. Der Code ist funktionsfähig; Sie erstellen jedoch eine zusätzliche Verbindung mit der Datenquelle, was sich negativ auf die Leistung auswirken kann.

When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source. To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file. In either case, set the provider to the provider name. For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

Die folgende Zeichenfolge stellt eine Verbindung mit einer lokalen Cubedatei am Speicherort\\C\\:\\MSDASDK\\Samples OLEDB OLAP\\Data\\bobsvid. Cub her:

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

