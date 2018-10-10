---
title: Der OLE DB-Anbieter für Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9f8fbed638c07e55b3ecb1730633dceee2b5c7e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473039"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a>Der OLE DB-Anbieter für Internet Publishing


**Betrifft**: Access 2013 | Office 2013

Die ADO-Objekte [Record](record-object-ado.md) und [Stream](stream-object-ado.md) können mit dem Microsoft OLE DB-Anbieter für Internet Publishing (Internet Publishing-Anbieter) verwendet werden, um auf Ressourcen (z. B. Webordner oder von Microsoft FrontPage bediente Dateien) zuzugreifen oder Ressourcen zu bearbeiten. Mit ADO können Sie die Quelle eines **Record** -, **Stream** - oder [Recordset](recordset-object-ado.md)-Objekts als URL angeben. Anschließend können Sie Ressourcen hochladen, herunterladen, verschieben, kopieren oder löschen oder Ressourceneigenschaften direkt bearbeiten.

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

