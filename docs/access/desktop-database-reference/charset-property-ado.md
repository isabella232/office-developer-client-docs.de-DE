---
<<<<<<< HEAD-Titel: Charset-Eigenschaft (ADO) TOCTitle: Charset-Eigenschaft (ADO) === Titel: Charset-Eigenschaft (ADO) TOCTitle: Charset-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15) Ms:contentKeyID: 48544551 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="charset-property-ado"></a>Charset-Eigenschaft (ADO)
=======
# <a name="charset-property-ado"></a>Charset-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den Zeichensatz an, in den der Inhalt eines Textdatenstroms übersetzt werden soll, um ihn im internen Puffer des Stream-Objekts zu speichern.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt fest oder gibt einen **String** -Wert, der angibt, in den der Inhalt des **Datenstroms** übersetzt werden, werden den Zeichensatz. Der Standardwert lautet "Unicode". Zulässige Werte sind typische Zeichenfolgen, die über die Schnittstelle übergeben, wie Internet-Zeichenfolgen Zeichensatz (z. B. "Iso-8859-1", "Windows-1252" Etc.). Eine Liste mit den Satz Zeichenfolgen, die von einem System bekannt ist, finden Sie unter der Unterschlüssel des HKEY\_Klassen\_ROOT\\MIME\\Datenbank\\Charset in der Windows-Registrierung.

## <a name="remarks"></a>Hinweise

In einem **Stream** -Textobjekt werden Textdaten in dem durch die **Charset** -Eigenschaft angegebenen Zeichensatz gespeichert. Der Standard ist Unicode. Mithilfe der **Charset** -Eigenschaft werden Daten konvertiert, die an das **Stream** -Objekt übertragen werden oder vom **Stream** -Objekt ausgehen. Wenn z. B. das **Stream** -Objekt ISO-8859-1-Daten enthält und diese zu einem BSTR kopiert werden, konvertiert das **Stream** -Objekt die Daten in Unicode. Dies gilt auch im umgekehrten Fall.

Für ein geöffnetes **Stream** -Objekt muss die aktuelle [Position](position-property-ado.md) am Beginn des **Stream** -Objekts (0) sein, damit **Charset** festgelegt werden kann.

**Charset** wird nur für **Stream**-Textobjekte ([Type](type-property-ado-stream.md) ist **adTypeText**) verwendet. Diese Eigenschaft wird ignoriert, wenn **Type** gleich **adTypeBinary** ist.

