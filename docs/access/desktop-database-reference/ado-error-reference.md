---
title: ADO-Fehlerreferenz
TOCTitle: ADO Error Reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8c1308b084efbf68233e9647cfed26d905d56400
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878773"
---
# <a name="ado-error-reference"></a>ADO-Fehlerreferenz


**Betrifft**: Access 2013, Office 2013

Die **ErrorValueEnum** -Konstante beschreibt die ADO-Fehlerwerte. Eine vollständige Aufstellung dieser aufgezählten Konstanten, einschließlich Werten, finden Sie in [Anhang B: ADO-Fehler](appendix-b-ado-errors.md). In diesem Abschnitt werden einige der interessanteren Fehler betrachtet. Außerdem werden Situationen, in denen diese ausgelöst werden können, oder Lösungen zum Beheben des Problems erläutert. Die **ErrorValueEnum** -Konstante und die Kurzform als positive Dezimalzahl werden aufgelistet.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nummer</p></th>
<th><p>ErrorValueEnum-Konstante</p></th>
<th><p>Beschreibung/mögliche Ursachen</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>Der Anbieter konnte den angeforderten Vorgang nicht ausführen.</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>Die Argumente haben den falschen Datentyp, liegen außerhalb des gültigen Bereichs oder stehen miteinander in Konflikt. Dieser Fehler wird häufig durch einen Tippfehler in einer SELECT-Anweisung von SQL verursacht. Beispielsweise kann dieser Fehler durch einen falsch geschriebenen Feldnamen oder Tabellennamen generiert werden. Dieser Fehler kann auch auftreten, wenn ein Feld oder eine Tabelle, das bzw. die in einer SELECT-Anweisung angegeben ist, im Datenspeicher nicht vorhanden ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>Die Datei konnte nicht geöffnet werden. Ein falsch geschriebener Dateiname wurde angegeben, oder eine Datei wurde verschoben, umbenannt oder gelöscht. Möglicherweise war über ein Netzwerk das Laufwerk vorübergehend nicht verfügbar, oder der Netzwerkverkehr verhinderte eine Verbindung.</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>Die Datei konnte nicht gelesen werden. Der Name der Datei ist falsch angegeben, die Datei wurde möglicherweise verschoben oder gelöscht, oder die Datei wurde beschädigt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>Fehler beim Schreiben in die Datei. Möglicherweise haben Sie eine Datei geschlossen und dann versucht in diese zu schreiben, oder die Datei ist beschädigt. Wenn sich die Datei auf einem Netzlaufwerk befindet, können vorübergehende Netzwerkbedingungen das Schreiben auf ein Netzlaufwerk verhindern.</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p>Entweder ist <strong>BOF</strong> oder <strong>EOF</strong> „True", oder der aktuelle Datensatz wurde gelöscht. Für den angeforderten Datensatz ist ein aktueller Datensatz erforderlich. Es wurde versucht, Datensätze mithilfe von <strong>Find</strong> oder <strong>Seek</strong> zu aktualisieren, um den Datensatzzeiger auf den gewünschten Datensatz zu verschieben. Wenn der Datensatz nicht gefunden wird, ist <strong>EOF</strong> gleich „True". Dieser Fehler kann auch nach einem Fehler bei der Methode <strong>AddNew</strong> oder <strong>Delete</strong> auftreten, weil kein aktueller Datensatz vorhanden ist, wenn diese Methoden einen Fehler erzeugen.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>Der Vorgang ist in diesem Zusammenhang nicht zulässig.</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>Der bereitgestellte Anbieter unterscheidet sich von dem bereits verwendeten Anbieter.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>Das <strong>Connection</strong> -Objekt kann während einer Transaktion nicht explizit geschlossen werden. Ein <strong>Recordset</strong> - oder <strong>Connection</strong> -Objekt, das derzeit an einer Transaktion beteiligt ist, kann nicht geschlossen werden. Rufen Sie <strong>RollbackTrans</strong> oder <strong>CommitTrans</strong> vor dem Schließen des Objekts auf.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>Das Objekt oder der Anbieter kann den angeforderten Vorgang nicht ausführen. Einige Vorgänge hängen von einer bestimmten Anbieterversion ab.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>Das Element, das dem angeforderten Namen oder der angeforderten Zahl entspricht, wurde in der Auflistung nicht gefunden. Ein falscher Feld- oder Tabellenname wurde angegeben.</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>Das Objekt ist bereits in der Auflistung vorhanden. Das Anfügen ist nicht möglich. Ein Objekt kann nicht zweimal derselben Auflistung hinzugefügt werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>Das Objekt ist nicht mehr gültig.</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>Die Anwendung verwendet für den aktuellen Vorgang einen Wert des falschen Datentyps. Beispielsweise könnten Sie für einen Vorgang, der einen Datenstrom erwartet, eine Zeichenfolge eingegeben haben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>Der Vorgang ist nicht zulässig, wenn das Objekt geschlossen ist. Das Objekt <strong>Connection</strong> oder <strong>Recordset</strong> wurde geschlossen. Beispielsweise könnte ein globales Objekt durch eine andere Routine geschlossen worden sein. Sie können diesen Fehler verhindern, indem Sie die <strong>State</strong> -Eigenschaft überprüfen, bevor Sie einen Vorgang auszuführen versuchen.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>Der Vorgang ist nicht zulässig, wenn das Objekt geöffnet ist. Ein geöffnetes Objekt kann nicht geöffnet werden. An ein geöffnetes <strong>Recordset</strong> -Objekt können keine Felder angefügt werden.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>Der Anbieter wurde nicht gefunden. Möglicherweise wurde er nicht ordnungsgemäß installiert. Möglicherweise wurde der Name des Anbieters falsch angegeben, der angegebene Anbieter ist nicht auf dem Computer installiert, auf dem der Code ausgeführt wird, oder die Installation wurde beschädigt.</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>Die <strong>ActiveConnection</strong> -Eigenschaft eines <strong>Recordset</strong> -Objekts, das ein <strong>Command</strong> -Objekt als Quelle aufweist, kann nicht geändert werden. Die Anwendung versuchte, ein neues <strong>Connection</strong> -Objekt einem <strong>Recordset</strong> -Objekt zuzuweisen, das ein <strong>Command</strong> -Objekt als Quelle aufweist.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>Das <strong>Parameter</strong> -Objekt ist nicht ordnungsgemäß definiert. Inkonsistente oder unvollständige Informationen wurden eingegeben.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>Die Verbindung kann nicht für diesen Vorgang verwendet werden. Die Verbindung ist entweder geschlossen oder in diesem Kontext ungültig.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>Der Vorgang kann während der Verarbeitung des Ereignisses nicht ausgeführt werden. Ein Vorgang kann innerhalb eines Ereignishandlers, durch den das Ereignis erneut ausgelöst wird, nicht ausgeführt werden. Beispielsweise sollten Navigationsmethoden nicht innerhalb eines <strong>WillMove</strong> -Ereignishandlers aufgerufen werden.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>Der Vorgang kann im asynchronen Modus nicht ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>Der Vorgang wurde vom Benutzer abgebrochen. Die Anwendung hat die Methode <strong>CancelUpdate</strong> oder <strong>CancelBatch</strong> aufgerufen, und der aktuelle Vorgang wurde abgebrochen.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>Der Vorgang kann für eine asynchrone Verbindung nicht ausgeführt werden.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>Die Koordinierungstransaktion ist ungültig oder wurde nicht gestartet.</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>Der Vorgang kann nicht verarbeitet werden, wenn er nicht ausgeführt wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>Die Sicherheitseinstellungen dieses Computers lassen den Zugriff auf eine Datenquelle in einer anderen Domäne nicht zu.</p></td>
</tr>
<tr class="even">
<td><p><strong>3717</strong></p></td>
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>Nur für die interne Verwendung. Verwenden Sie diese Konstante nicht. (Der Eintrag ist der Vollständigkeit halber enthalten; dieser Fehler sollte im Code nicht angezeigt werden.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>3718</strong></p></td>
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>Nur für die interne Verwendung. Verwenden Sie diese Konstante nicht. (Der Eintrag ist der Vollständigkeit halber enthalten; dieser Fehler sollte im Code nicht angezeigt werden.)</p></td>
</tr>
<tr class="even">
<td><p><strong>3719</strong></p></td>
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>Der Datenwert steht in Konflikt mit den Integritätseinschränkungen des Felds. Ein neuer Wert für ein <strong>Field</strong> -Objekt würde zu einem doppelten Schlüssel führen. Ein Wert, der eine Seite einer Beziehung zwischen zwei Datensätzen darstellt, kann möglicherweise nicht aktualisiert werden.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>Unzureichende Berechtigungen verhindern das Schreiben in das Feld. Der in der Verbindungszeichenfolge genannte Benutzer hat nicht die erforderlichen Berechtigungen, um in ein <strong>Field</strong> -Objekt zu schreiben.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>Der Datenwert ist zu groß, um vom Felddatentyp dargestellt zu werden. Ein numerischer Wert wurde zugewiesen, der für das beabsichtigte Feld zu groß ist. Beispielsweise wurde ein Wert vom Typ Long Integer einem Feld vom Typ Short Integer zugewiesen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>Der Datenwert steht in Konflikt mit dem Datentyp oder mit Einschränkungen des Felds. Der Datenspeicher weist Gültigkeitseinschränkungen auf, die vom Wert des <strong>Field</strong> -Objekts abweichen.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>Fehler bei der Konvertierung, da der Datenwert ein Vorzeichen hat, der vom Anbieter verwendete Felddatentyp aber kein Vorzeichen aufweist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>Der Datenwert kann aus anderen Gründen als einem Vorzeichenkonflikt oder einem Datenüberlauf nicht konvertiert werden. Beispielsweise könnten bei der Konvertierung Daten abgeschnitten werden.</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>Der Datenwert kann nicht festgelegt oder abgerufen werden, da der Felddatentyp unbekannt war, oder der Anbieter verfügte über unzureichende Ressourcen zum Ausführen des Vorgangs.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>Der Datensatz enthält dieses Feld nicht. Ein falscher Feldname wurde angegeben, oder es wurde auf ein Feld verwiesen, das nicht in der <strong>Fields</strong> -Auflistung des aktuellen Datensatzes vorhanden ist.  </p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>Entweder die Quell-URL oder das übergeordnete Element der Ziel-URL ist nicht vorhanden. In der Quell- oder Ziel-URL ist ein Tippfehler vorhanden. Sie müssen möglicherweise https://mysite/photo/myphoto.jpg Wenn sollten Sie tatsächlich haben https://mysite/photos/myphoto.jpg stattdessen. Der Tippfehler in der übergeordneten URL (in diesem Fall <em>Foto</em> anstelle von <em>Fotos</em>) hat den Fehler verursacht hat.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>Unzureichende Berechtigungen für den Zugriff auf die Struktur oder die Unterstruktur. Der in der Verbindungszeichenfolge genannte Benutzer hat nicht die erforderlichen Berechtigungen.</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>Die URL enthält ungültige Zeichen. Stellen Sie sicher, dass die URL richtig eingegeben ist. Die URL folgt dem für den aktuellen Anbieter registrierten Schema (z. B. ist der Internet Publishing-Anbieter für HTTP registriert).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>Das von der angegebenen URL dargestellte Objekt ist von mindestens einem anderen Prozess gesperrt. Warten Sie, bis der Prozess abgeschlossen wurde, und wiederholen Sie dann den Vorgang. Das Objekt, auf das Sie zuzugreifen versuchen, wurde von einem anderen Benutzer oder einem anderen Prozess in Ihrer Anwendung gesperrt. Diese Situation ist in einer Mehrbenutzerumgebung am wahrscheinlichsten.</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>Der Kopiervorgang kann nicht ausgeführt werden. Das durch die Ziel-URL genannte Objekt ist bereits vorhanden. Geben Sie <strong>AdCopyOverwrite</strong> an, um das Objekt zu ersetzen. Falls Sie <strong>AdCopyOverwrite</strong> beim Kopieren von Dateien in ein Verzeichnis nicht angeben, wird beim Kopieren ein Fehler erzeugt, wenn Sie versuchen, ein im Zielordner bereits vorhandenes Element zu kopieren.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>Der Server kann den Vorgang nicht abschließen. Dies könnte darauf zurückzuführen sein, dass der Server mit anderen Vorgängen ausgelastet ist oder unzureichende Ressourcen aufweist.</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>Der Anbieter konnte das von der URL angegebene Speichergerät nicht finden. Stellen Sie sicher, dass die URL richtig eingegeben ist. Die URL des Speichergeräts stimmt möglicherweise nicht, aber dieser Fehler kann auch andere Ursachen haben. Das Gerät war möglicherweise offline, oder das Herstellen der Verbindung wurde durch hohen Netzwerkverkehr verhindert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>Der Vorgang kann nicht ausgeführt werden. Der Anbieter kann nicht genügend Speicherplatz abrufen. Möglicherweise gibt es für temporäre Dateien auf dem Server nicht genügend Arbeitsspeicher (RAM) oder freien Speicherplatz.</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>Die Quell- oder Ziel-URL liegt außerhalb des Bereichs des aktuellen Datensatzes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>Der Vorgang konnte nicht abgeschlossen werden, und der Status ist nicht verfügbar. Möglicherweise ist das Feld nicht verfügbar, oder der Vorgang wurde nicht ausgeführt. Ein anderer Benutzer hat möglicherweise das Feld, auf das Sie zuzugreifen versuchen, geändert oder gelöscht.</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>Der von dieser URL genannte Datensatz ist nicht vorhanden. Beim Öffnen einer Datei mithilfe eines <strong>Record</strong> -Objekts war entweder der Dateiname oder der Pfad zur Datei falsch geschrieben.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>Die URL des Objekts, das gelöscht werden soll, liegt außerhalb des Bereichs des aktuellen Datensatzes.</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>Für den Vorgang ist ein gültiger <strong>ParentCatalog</strong> erforderlich.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>Die Verbindung wurde verweigert. Die angeforderte neue Verbindung weist andere Merkmale als die bereits verwendete Verbindung auf.</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>Fehler beim Aktualisieren von Feldern. Weitere Informationen erhalten Sie in der <strong>Status</strong> -Eigenschaft einzelner Feldobjekte. Dieser Fehler kann in zwei Situationen auftreten: beim Ändern des Werts eines <strong>Field</strong> -Objekt während des Änderns oder Hinzufügens eines Datensatzes zur Datenbank und beim Ändern der Eigenschaften des <strong>Field</strong> -Objekts selbst. Die Aktualisierung von <strong>Record</strong> oder <strong>Recordset</strong> ist aufgrund eines Problems mit einem der Felder im aktuellen Datensatz fehlgeschlagen. Zählen Sie die <strong>Fields</strong> -Auflistung auf, und überprüfen Sie die <strong>Status</strong> -Eigenschaft für jedes Feld, um die Ursache des Problems zu ermitteln.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>Der Anbieter unterstützt Freigabeeinschränkungen nicht. Es wurde versucht, die Dateifreigabe einzuschränken, aber dies wird vom Anbieter nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>Der Anbieter unterstützt die angeforderte Art von Freigabeeinschränkung nicht. Es wurde versucht, einen bestimmten Typ von Dateifreigabeeinschränkung einzurichten, der von Ihrem Anbieter nicht unterstützt wird. In der Dokumentation des Anbieters finden Sie Informationen, welche Dateifreigabeeinschränkungen unterstützt werden.</p></td>
</tr>
</tbody>
</table>

