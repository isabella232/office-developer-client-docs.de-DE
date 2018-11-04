---
title: Open-Methode (ADO-Verbindung)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66a62128a8ad8828c501cdaf899448edd9f1d37f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949873"
---
# <a name="open-method-ado-connection"></a>Open-Methode (ADO-Verbindung)

**Betrifft**: Access 2013, Office 2013
 
Eine Verbindung mit einer Datenquelle wird geöffnet.

## <a name="syntax"></a>Syntax

*Verbindung*. Öffnen Sie*ConnectionString*, *UserID*, *Kennwort*, *Optionen*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectionString* |Optional. Ein **String** -Wert, der Verbindungsinformationen enthält. Details zu den gültigen Einstellungen finden Sie unter der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft.|
|*UserID* |Optional. Ein **String** -Wert, der einen Benutzernamen enthält, der beim Herstellen der Verbindung verwendet werden soll.|
|*Password* |Optional. Ein **String** -Wert, der ein Kennwort enthält, das beim Herstellen der Verbindung verwendet werden soll.|
|*Options* |Optional. Ein [ConnectOptionEnum](connectoptionenum.md)-Wert, durch den festgelegt wird, dass diese Methode nach (synchron) oder vor (asynchron) dem Herstellen der Verbindung zurückgegeben wird.|

## <a name="remarks"></a>Hinweise

Durch Verwenden der **Open** -Methode für ein [Connection](connection-object-ado.md)-Objekt wird die physische Verbindung mit einer Datenquelle hergestellt. Nach dem erfolgreichen Abschluss dieser Methode ist die Verbindung aktiv, und Sie können Befehle für sie ausgeben und die Ergebnisse verarbeiten.

Verwenden Sie das optionale Argument *ConnectionString* , um entweder eine Verbindungszeichenfolge fest, die mit einer Reihe von durch Semikolons oder eine Datei getrennte *Argument* *= Wert* Anweisungen oder Directory-Ressource mit einer URL identifiziert anzugeben. Die **ConnectionString** -Eigenschaft erbt automatisch den Wert für das Argument *ConnectionString* verwendet. Aus diesem Grund kann entweder die **ConnectionString** -Eigenschaft des **Connection** -Objekts festlegen, bevor Sie ihn öffnen, oder verwenden Sie das Argument *ConnectionString* festzulegen oder außer Kraft setzen die aktuellen Verbindungsparameter während des Aufrufs der **Open** -Methode .

Wenn Sie Benutzer- und Kennwortinformationen sowohl im *ConnectionString*-Argument als auch in den optionalen Argumenten *UserID* und *Password* übergeben, werden durch die Argumente *UserID* und *Password* die in *ConnectionString* angegebenen Werte außer Kraft gesetzt.

Wenn Sie die Operationen über eine offene **Verbindung** abgeschlossen haben, verwenden Sie die [Close](close-method-ado.md)-Methode, um zugeordnete Systemressourcen freizugeben. Durch das Schließen eines Objekts wird dieses nicht aus dem Speicher entfernt. Sie können seine Eigenschafteneinstellungen ändern und es später mit der **Open**-Methode erneut öffnen. Legen Sie die Objektvariable auf *Nothing* fest, um ein Objekt vollständig aus dem Speicher zu entfernen.

**Remote Data Service-Verwendung** Wenn für ein clientseitiges **Connection** -Objekt verwendet, herstellen nicht die **Open** -Methode tatsächlich eine Verbindung mit dem Server, bis ein [Recordset-Objekt](recordset-object-ado.md) für das **Connection** -Objekt geöffnet wird.

> [!NOTE]
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).


