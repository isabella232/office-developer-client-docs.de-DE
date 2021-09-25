---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f087e5fd301ade7331a3681be6042ec61b48493c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596449"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Empfängereintrag mit Daten, die sich in einem Hostadressbuchanbieter befinden.
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parameter

 _cbTemplateID_
  
> [in] Die Byteanzahl im Vorlagenbezeichner, auf die der  _lpTemplateID-Parameter_ verweist. 
    
 _lpTemplateID_
  
> [in] Ein Zeiger auf die Vorlagen-ID oder **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft des Empfängereintrags, der geöffnet werden soll.
    
 _ulTemplateFlags_
  
> [in] Eine Bitmaske mit Flags, die angibt, wie der durch den Vorlagenbezeichner dargestellte Eintrag geöffnet wird. Das folgende Kennzeichen kann festgelegt werden:
    
FILL_ENTRY 
  
> Der Hostanbieter erstellt einen neuen Eintrag in seinem Container basierend auf dem Eintrag, der durch den Vorlagenbezeichner dargestellt wird. Die **IABLogon::OpenTemplateID-Methode** sollte entweder eine bestimmte Initialisierung des Hostanbietereintrags mithilfe der [IMAPIProp:IUnknown-Implementierung](imapipropiunknown.md) im  _lpMAPIPropData-Parameter_ ausführen oder eine benutzerdefinierte **IMAPIProp-Schnittstellenimplementierung** im  _lppMAPIPropNew-Parameter_ zurückgeben. 
    
 _lpMAPIPropData_
  
> [in] Ein Zeiger auf das Eigenschaftsobjekt des Hostanbieters und die Implementierung einer Schnittstelle, die von **IMAPIProp** abgeleitet wurde.
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der den Typ des Schnittstellenzeigers darstellt, der im  _lppMAPIPropNew-Parameter_ zurückgegeben werden soll. Wenn **Null** übergeben wird, wird die standardmäßige Messaging-Benutzeroberfläche [IMailUser : IMAPIProp](imailuserimapiprop.md)zurückgegeben.
    
 _lppMAPIPropNew_
  
> [out] Ein Zeiger auf das gebundene Eigenschaftsobjekt und eine Implementierung einer Schnittstelle, die von **IMAPIProp** abgeleitet wird.
    
 _lpMAPIPropSibling_
  
> [out] Reserviert; muss **NULL** sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der entsprechende Code wurde erfolgreich an verwandte Daten im Hostanbieter gebunden.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine Vorlagen-IDs.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der im  _lpTemplateID-Parameter übergebene_ Vorlagenbezeichner wird vom Adressbuchanbieter nicht erkannt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IABLogon::OpenTemplateID-Methode** wird nur von Adressbuchanbietern implementiert, die die Kontrolle über Kopien ihrer Einträge behalten müssen, die sich in den Containern von Hostanbietern befinden. Anbieter, die **OpenTemplateID** implementieren, werden als fremder Adressbuchanbieter bezeichnet. Hostanbieter rufen [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) auf, um einen kopierten Eintrag zu erstellen oder den kopierten Eintrag zu öffnen, und MAPI übergibt den Aufruf an **IABLogon::OpenTemplateID.** **IABLogon::OpenTemplateID** öffnet den Eintrag und bindet den Code, der ihn steuert, an Daten im Hostanbieter. 
  
Statt einen Eintragsbezeichner zu verwenden, verwendet **IABLogon::OpenTemplateID** eine andere Eigenschaft, den Vorlagenbezeichner des **Eintrags, PR_TEMPLATEID**. Vorlagenbezeichner sollten für Einträge unterstützt werden, deren Code an Daten in einem Hostanbieter gebunden werden muss.
  
Beispiele für die Implementierung von **IABLogon::OpenTemplateID** durch einen Adressbuchanbieter sind: 
  
- So aktualisieren Sie in regelmäßigen Abständen die Daten für einen kopierten Eintrag, damit sie mit dem Original synchronisiert bleiben.
    
- Zum Implementieren von Funktionen, die der Hostanbieter nicht implementieren kann, z. B. dynamisches Auffüllen einer Liste, die in der Detailtabelle des Eintrags aus Daten auf einem Server angezeigt wird.
    
- Um die Interaktion zwischen Eigenschaften im Eintrag des Hostanbieters und dem ursprünglichen Eintrag zu steuern, z. B. das Berechnen der **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) anhand der Werte der Bearbeitungssteuerelemente in der Detailanzeige, die verschiedene Komponenten der Adresse enthalten.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Hostanbieter einen Eintrag von Ihrem Anbieter kopiert oder erstellt und Sie eine Implementierung eines Eigenschaftsobjekts über **IABLogon::OpenTemplateID** bereitstellen, verarbeiten Sie die meisten Aufrufe, um den Eintrag zu verwalten. Da es jedoch aufgabe des Hostanbieters ist, diese Anrufe an Sie weiterzuleiten, kann der Hostanbieter jeden Anruf abfangen und eine benutzerdefinierte Verarbeitung durchführen, bevor der Anruf weitergeleitet wird.
  
Sie sollten die folgenden Richtlinien in Den Property-Objektimplementierungen verwenden:
  
- Wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird, bestimmen Sie, ob es sich bei der Anforderung um eine berechnete Eigenschaft handelt, und behandeln Sie sie, falls ja. Übertragen Sie alle Anforderungen für nicht kompatible Eigenschaften an den Hostanbieter. 
    
- Wenn [IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufgerufen wird, um eine beliebige Tabelle mit Ausnahme der Detailanzeigetabelle zu öffnen, behandeln Sie die Anforderung. Die meisten Tabellen können nicht exakt in den Hostanbieter kopiert werden. Sie müssen die **IMAPITable-Implementierung** für diese angeforderten Tabellen generieren. Die Detailtabelle **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft muss in den Hostanbieter kopiert werden. Dadurch kann dieser Anbieter die Tabelle lokal generieren. Möglicherweise möchten Sie die Implementierung der Anzeigetabelle umschließen, um Benachrichtigungen über Anzeigetabellen zu generieren. 
    
- Wenn [IMAPIProp::SetProps](imapiprop-setprops.md) aufgerufen wird, kann der Hostanbieter die Daten überprüfen, bevor Sie die Eigenschaften festlegen können. Sie können überprüfen, ob alle erforderlichen Eigenschaften festgelegt oder berechnet wurden. Wenn ein Fehler erkannt wird, geben Sie den entsprechenden Fehlerwert und, falls möglich, eine zusätzliche Erklärung über [IMAPIProp::GetLastError zurück.](imapiprop-getlasterror.md)
    
- Wenn [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird, kann der Hostanbieter die Verarbeitung durchführen, bevor Sie den Eintrag speichern. Sie sollten alle Daten, die von den geänderten Eigenschaften betroffen sind, z. B. eine neue Adresse, im Eintrag des Hostanbieters speichern. 
    
Im Allgemeinen müssen Sie bei der Implementierung des Eintrags, den Sie an den Hostanbieter übergeben, alle Methoden abfangen, um kontextspezifische Manipulationen der relevanten Eigenschaften durchzuführen. Wenn das FILL_ENTRY Flag im  _ulTemplateFlags-Parameter_ übergeben wird, legen Sie alle Eigenschaften für den Eintrag fest. 
  
Wenn Sie ein neues Eigenschaftsobjekt im  _Parameter "lppMAPIPropNew"_ zurückgeben, rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) des Eigenschaftsobjekts des Hostanbieters auf, um einen Verweis aufrechtzuerhalten. Alle Aufrufe über das gebundene Objekt, das von der in _lppMAPIPropNew_ zurückgegebenen **IMAPIProp-Implementierung** zurückgegeben wird, sollten an die entsprechende Methode im Hosteigenschaftsobjekt weitergeleitet werden, nachdem sie vom gebundenen Objekt behandelt wurden. 
  
Die Eigenschaftsbezeichner aller benannten Eigenschaften, die über das gebundene Eigenschaftsobjekt übergeben werden, befinden sich im Bezeichnernamespace des Anbieters. Ihre Implementierung der [IMAPIProp::GetNamesFromIDs-Methode](imapiprop-getnamesfromids.md) sollte die Namen der Eigenschaften bestimmen, damit sie vorlagenspezifische Aufgaben ausführen kann. Ebenso müssen Eigenschaften, die der Anbieter an den Hostanbieter übergibt, auch in Ihrem Namespace enthalten sein. Wenn Sie z. B. eine benannte Eigenschaft in **OpenTemplateID** festlegen, sollten Sie einen Ihrer Bezeichner für den Namen verwenden, der bei Bedarf durch Aufrufen der [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) erstellt wird. 
  
Wenn Sie den in  _lpTemplateID übergebenen_ Eintragsbezeichner nicht erkennen, geben Sie MAPI_E_UNKNOWN_ENTRYID zurück.
  
Weitere Informationen zum Arbeiten mit Adressbuchvorlagenbezeichnern finden Sie unter [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid (kanonische Eigenschaft)](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

