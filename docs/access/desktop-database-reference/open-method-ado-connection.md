---
title: Open-Methode (ADO-Verbindung)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 45d41395759039fa664caeb5950931e8e39e3cc4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558184"
---
# <a name="open-method-ado-connection"></a>Open-Methode (ADO-Verbindung)

**Gilt für**: Access 2013, Office 2013
 
Eine Verbindung mit einer Datenquelle wird geöffnet.

## <a name="syntax"></a>Syntax

*connection*. Open *ConnectionString*, *UserID*, *Password*, *Options*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectionString* |Optional. Ein **String** -Wert, der Verbindungsinformationen enthält. Details zu den gültigen Einstellungen finden Sie unter der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft.|
|*UserID* |Optional. Ein **String** -Wert, der einen Benutzernamen enthält, der beim Herstellen der Verbindung verwendet werden soll.|
|*Password* |Optional. Ein **String** -Wert, der ein Kennwort enthält, das beim Herstellen der Verbindung verwendet werden soll.|
|*Options* |Optional. Ein [ConnectOptionEnum](connectoptionenum.md)-Wert, durch den festgelegt wird, dass diese Methode nach (synchron) oder vor (asynchron) dem Herstellen der Verbindung zurückgegeben wird.|

## <a name="remarks"></a>HinwBemerkungeneise

Durch Verwenden der **Open**-Methode für ein [Connection](connection-object-ado.md)-Objekt wird die physische Verbindung mit einer Datenquelle hergestellt. Nach dem erfolgreichen Abschluss dieser Methode ist die Verbindung aktiv, und Sie können Befehle für sie ausgeben und die Ergebnisse verarbeiten.

Verwenden Sie das optionale *ConnectionString-Argument,* um entweder eine Verbindungszeichenfolge anzugeben, die eine Reihe von *Argumenten* = durch Semikolons getrennte *Wertanweisungen* enthält, oder eine Datei- oder Verzeichnisressource, die mit einer URL identifiziert wird. Die **ConnectionString**-Eigenschaft erbt automatisch den für das *ConnectionString*-Argument verwendeten Wert. Daher können Sie die **ConnectionString**-Eigenschaft des **Connection**-Objekts festlegen, bevor Sie es öffnen, oder das *ConnectionString*-Argument verwenden, um die aktuellen Verbindungsparameter während des Aufrufs der **Open**-Methode festzulegen oder außer Kraft zu setzen.

Wenn Sie Benutzer- und Kennwortinformationen sowohl im *ConnectionString*-Argument als auch in den optionalen Argumenten *UserID* und *Password* übergeben, werden durch die Argumente *UserID* und *Password* die in *ConnectionString* angegebenen Werte außer Kraft gesetzt.

Wenn Sie die Operationen über eine offene **Verbindung** abgeschlossen haben, verwenden Sie die [Close](close-method-ado.md)-Methode, um zugeordnete Systemressourcen freizugeben. Durch das Schließen eines Objekts wird dieses nicht aus dem Speicher entfernt. Sie können seine Eigenschafteneinstellungen ändern und es später mit der **Open**-Methode erneut öffnen. Legen Sie die Objektvariable auf *Nothing* fest, um ein Objekt vollständig aus dem Speicher zu entfernen.

**Remote data service usage** Bei Verwendung in einem clientseitigen **Connection-Objekt** stellt die **Open-Methode** erst dann eine Verbindung mit dem Server her, wenn ein [Recordset-Objekt](recordset-object-ado.md) für das **Connection-Objekt** geöffnet wird.

> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)


