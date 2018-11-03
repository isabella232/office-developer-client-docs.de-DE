---
title: Der OLE DB-Anbieter für Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 536acebd305927cffe50e742245be97a48242796
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945748"
---
# <a name="ole-db-provider-for-internet-publishing"></a>OLE DB-Anbieter für Internet Publishing


**Betrifft**: Access 2013, Office 2013

Die ADO- [Record](record-object-ado.md) und [Stream](stream-object-ado.md) -Objekten können verwendet werden mit dem Microsoft OLE DB-Anbieter für Internet Publishing (Internet Publishing-Anbieter) aufrufen und Bearbeiten von Ressourcen, wie von Webordnern oder Dateien, die von Microsoft FrontPage bedient. Mit ADO können Sie die Quelle der **Datensatz**, **Stream**oder [Recordset-Objekt](recordset-object-ado.md) eine URL sein soll, angeben. Sie können dann hochladen, herunterladen, verschieben, kopieren, und Löschen von Ressourcen oder Ressourceneigenschaften direkt zu bearbeiten.

Beispielcode, bei dem die Objekte **Record** und **Stream** mit dem Internet Publishing-Anbieter verwendet werden, finden Sie unter [Internet Publishing-Szenario](internet-publishing-scenario.md).

Der Internet Publishing-Anbieter wird mit Microsoft Windows 2000 installiert. Frühere Versionen des Internet Publishing-Anbieters sind auch mit Microsoft Office 2000 und Microsoft Internet Explorer 5.0 verfügbar.

Sie haben drei Möglichkeiten, ADO mit dem Internet Publishing-Anbieter zu verbinden:

- Geben Sie "URL=" in der Verbindungszeichenfolge an. Beispiel:
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Geben Sie Msdaipp.dso für das Schlüsselwort Provider der Verbindungszeichenfolge an. Beispiel:

    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Geben Sie Msdaipp.dso für die Provider-Eigenschaft des Connection-Objekts an. Beispiel:

    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```


> [!NOTE]
> <P>Wenn Msdaipp.dso ausdrücklich als Wert für den Anbieter angegeben ist (mit dem Schlüsselwort Provider der Verbindungszeichenfolge oder mit der Provider-Eigenschaft) kann "URL=" nicht in der Verbindungszeichenfolge verwendet werden, da sonst ein Fehler auftritt. Geben Sie die URL stattdessen wie oben dargestellt an.</P>



Weitere Informationen zum Internet Publishing-Anbieter finden Sie unter [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) oder in der Dokumentation zum Anbieter der Quellanwendung, mit der der OLE DB-Anbieter für Internet Publishing installiert wurde: Windows 2000, Office 2000 oder Internet Explorer 5.0.

