---
title: Der OLE DB-Anbieter für Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7315df5a20cf032fc256f03893531f58857d470a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998665"
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
> Wenn Msdaipp.dso explizit als Wert des Anbieters, mit dem *Anbieter* Verbindungszeichenfolgen-Schlüsselworts oder der **Provider** -Eigenschaft angegeben ist kann nicht verwendet "URL =" in der Verbindungszeichenfolge. Wenn "URL=" dennoch verwendet wird, tritt ein Fehler auf. Geben Sie stattdessen einfach die URL wie weiter oben in diesem Thema dargestellt.

Weitere Informationen zum Internet Publishing-Anbieter finden Sie unter [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) oder in der Dokumentation zum Anbieter der Quellanwendung, mit der der OLE DB-Anbieter für Internet Publishing installiert wurde: Windows 2000, Office 2000 oder Internet Explorer 5.0.

