---
title: Der OLE DB-Anbieter für Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 22735ede3150b8735902fb94e5b774df41592dca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593453"
---
# <a name="ole-db-provider-for-internet-publishing"></a>OLE DB-Anbieter für Internet Publishing

**Gilt für**: Access 2013, Office 2013

Die ADO [Record-](record-object-ado.md) und [Stream-Objekte](stream-object-ado.md) können mit dem Microsoft OLE DB-Anbieter für Internet Publishing (Internet Publishing Provider) verwendet werden, um auf Ressourcen zuzugreifen und diese zu bearbeiten, z. B. Webordner oder Dateien, die von Microsoft FrontPage bereitgestellt werden. Mit ADO können Sie die Quelle eines **Record**-, **Stream**- oder [Recordset](recordset-object-ado.md)-Objekts als URL angeben. Anschließend können Sie Ressourcen hochladen, herunterladen, verschieben, kopieren oder löschen oder Ressourceneigenschaften direkt bearbeiten.

Beispielcode, bei dem die Objekte **Record** und **Stream** mit dem Internet Publishing-Anbieter verwendet werden, finden Sie unter [Internet Publishing-Szenario](internet-publishing-scenario.md).

Der Internet Publishing-Anbieter wird mit Microsoft Windows 2000 installiert. Frühere Versionen des Internet Publishing-Anbieters sind auch mit Microsoft Office 2000 und Microsoft Internet Explorer 5.0 verfügbar.

Sie haben drei Möglichkeiten, ADO mit dem Internet Publishing-Anbieter zu verbinden:

- Geben Sie "URL=" in der Verbindungszeichenfolge an. Beispiel:
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Geben Sie Msdaipp.dso für das *Schlüsselwort Provider* der Verbindungszeichenfolge an. For example:
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object. For example:
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Wenn Msdaipp.dso explizit als Wert des Anbieters angegeben ist, entweder mit dem *Schlüsselwort* für die Anbieterverbindungszeichenfolge oder der **Provider-Eigenschaft,** können Sie "URL=" nicht in der Verbindungszeichenfolge verwenden. If you do, an error will occur. Geben Sie stattdessen einfach die URL an, wie weiter oben in diesem Thema gezeigt.

Weitere Informationen zum Internet Publishing-Anbieter finden Sie unter [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) oder in der Dokumentation zum Anbieter der Quellanwendung, mit der der OLE DB-Anbieter für Internet Publishing installiert wurde: Windows 2000, Office 2000 oder Internet Explorer 5.0.

