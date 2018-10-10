---
title: ActiveConnection-Eigenschaft (ADO MD)
TOCTitle: ActiveConnection Property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0743771ee9cee096f8de3d91d793ea8cf81af2ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475225"
---
# <a name="activeconnection-property-ado-md"></a>ActiveConnection-Eigenschaft (ADO MD)


**Betrifft**: Access 2013 | Office 2013

Gibt an, zu welchem ADO-[Connection](connection-object-ado.md)-Objekt die aktuelle Zellmenge oder der Katalog derzeit gehört.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **Variant** -Wert fest oder gibt diesen zurück. Der Wert enthält eine Zeichenfolge, die eine Verbindung oder ein **Connection** -Objekt definiert. Die Standardeinstellung ist eine leere Zeichenfolge.

## <a name="remarks"></a>Hinweise

Sie können diese Eigenschaft auf ein gültiges ADO- **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festlegen. Wenn diese Eigenschaft auf eine Verbindungszeichenfolge festgelegt wird, erstellt der Anbieter mithilfe dieser Definition ein neues **Connection** -Objekt und öffnet die Verbindung.

Wenn Sie das **ActiveConnection** -Argument der [Open](open-method-ado-md.md)-Methode verwenden, um ein [Cellset](cellset-object-ado-md.md)-Objekt zu öffnen, erbt die **ActiveConnection** -Eigenschaft den Wert des Arguments.

Beim Festlegen der **ActiveConnection** -Eigenschaft eines [Catalog](catalog-object-ado-md.md)-Objekts auf **Nothing** werden die verbundenen Daten freigegeben, einschließlich der Daten in der [CubeDefs](cubedefs-collection-ado-md.md)-Auflistung und der verbundenen [Dimension](dimension-object-ado-md.md)-, [Hierarchy](hierarchy-object-ado-md.md)-, [Level](level-object-ado-md.md)- und [Member](member-object-ado-md.md)-Objekte. Beim Schließen eines **Connection** -Objekts, das verwendet wurde, um ein **Catalog** -Objekt zu öffnen, wird dieselbe Wirkung wie beim Festlegen der **ActiveConnection** -Eigenschaft auf **Nothing** erzielt.

Durch Ändern der Standarddatenbank der Verbindung, auf die durch die **ActiveConnection** -Eigenschaft eines **Catalog** -Objekts verwiesen wurde, wird der Inhalt des **Catalog** -Objekts ungültig.

Wenn Sie versuchen, die **ActiveConnection** -Eigenschaft für ein geöffnetes **Cellset** -Objekt zu ändern, tritt ein Fehler auf.


> [!NOTE]
> <P>[!HINWEIS] Achten Sie in Visual Basic darauf, das <STRONG>Set</STRONG> -Schlüsselwort zu verwenden, wenn Sie die <STRONG>ActiveConnection</STRONG> -Eigenschaft auf ein <STRONG>Connection</STRONG> -Objekt festlegen. Wenn Sie das <STRONG>Set</STRONG> -Schlüsselwort nicht verwenden, legen Sie die <STRONG>ActiveConnection</STRONG> -Eigenschaft gleich der Standardeigenschaft des <STRONG>Connection</STRONG> -Objekts , <STRONG>ConnectionString</STRONG>, fest. Der Code ist funktionsfähig; Sie erstellen jedoch eine zusätzliche Verbindung mit der Datenquelle, was sich negativ auf die Leistung auswirken kann.</P>



Wenn Sie den MSOLAP-Datenanbieter verwenden, legen Sie die Datenquelle in einer Verbindungszeichenfolge auf einen Servernamen fest, und legen Sie für den ursprünglichen Katalog den Namen eines Katalogs aus der Datenquelle fest. Legen Sie als Speicherort den vollständigen Dateipfad der CUB-Datei fest, um eine Verbindung mit einer Cubedatei herzustellen, die von einen Server getrennt ist. Legen Sie in jedem Fall für den Anbieter den Anbieternamen fest. Mit der folgenden Zeichenfolge wird z. B. eine Verbindung mit dem Katalog Bobs Video Store auf dem Server Servername mit dem MSOLAP-Anbieter hergestellt:

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

Die folgende Zeichenfolge stellt eine Verbindung mit einer lokalen Cubedatei am Speicherort C:\\MSDASDK\\Beispiele\\Oledb\\Olap\\Daten\\bobsvid.cub:

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

