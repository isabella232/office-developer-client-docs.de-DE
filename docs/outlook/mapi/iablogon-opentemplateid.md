---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334748"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Empfängereintrag mit Daten in einem Host-Adressbuchanbieter.
  
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
  
> [in] Die Byteanzahl in der Vorlagen-ID, auf die der  _lpTemplateID-Parameter_ verweist. 
    
 _lpTemplateID_
  
> [in] Ein Zeiger auf die Vorlagen-ID oder **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des zu öffnenden Empfängereintrags.
    
 _ulTemplateFlags_
  
> [in] Eine Bitmaske mit Flags, mit der angegeben wird, wie der durch die Vorlagen-ID dargestellte Eintrag geöffnet wird. Das folgende Flag kann festgelegt werden:
    
FILL_ENTRY 
  
> Der Hostanbieter erstellt einen neuen Eintrag in seinem Container basierend auf dem Durch die Vorlagen-ID dargestellten Eintrag. Die **IABLogon::OpenTemplateID-Methode** sollte entweder eine bestimmte Initialisierung des Eintrags des Hostanbieters mithilfe der [IMAPIProp : IUnknown-Implementierung](imapipropiunknown.md) im  _lpMAPIPropData-Parameter_ durchführen oder eine benutzerdefinierte **IMAPIProp-Schnittstellenimplementierung** im  _lppMAPIPropNew-Parameter_ zurückgeben. 
    
 _lpMAPIPropData_
  
> [in] Ein Zeiger auf das Eigenschaftsobjekt des Hostanbieters und die Implementierung einer Schnittstelle, die von **IMAPIProp abgeleitet ist.**
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der den Typ des Schnittstellenzeigers darstellt, der im  _lppMAPIPropNew-Parameter zurückgegeben werden_ soll. Durch **Übergeben von null** wird die standardmäßige Messagingbenutzeroberfläche [IMailUser : IMAPIProp zurückgegeben.](imailuserimapiprop.md)
    
 _lppMAPIPropNew_
  
> [out] Ein Zeiger auf das gebundene Eigenschaftsobjekt und eine Implementierung einer Schnittstelle, die von **IMAPIProp abgeleitet ist.**
    
 _lpMAPIPropSibling_
  
> [out] Reserviert; muss **null sein.**
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der entsprechende Code wurde erfolgreich an verwandte Daten im Hostanbieter gebunden.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine Vorlagen-IDs.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der im  _lpTemplateID-Parameter_ übergebene Vorlagenbezeichner wird vom Adressbuchanbieter nicht erkannt. 
    
## <a name="remarks"></a>Hinweise

Die **IABLogon::OpenTemplateID-Methode** wird nur von Adressbuchanbietern implementiert, die die Kontrolle über Kopien ihrer Einträge behalten müssen, die sich in den Containern von Hostanbietern befinden. Anbieter, die **OpenTemplateID implementieren,** werden als fremde Adressbuchanbieter bezeichnet. Hostanbieter rufen [IMAPISupport::OpenTemplateID auf,](imapisupport-opentemplateid.md) um einen kopierten Eintrag zu erstellen oder den kopierten Eintrag zu öffnen, und MAPI übergibt den Aufruf an **IABLogon::OpenTemplateID**. **IABLogon::OpenTemplateID** öffnet den Eintrag und bindet den Code, der ihn steuert, an Daten im Hostanbieter. 
  
Anstatt einen Eintragsbezeichner zu verwenden, verwendet **IABLogon::OpenTemplateID** eine andere Eigenschaft, den Vorlagenbezeichner des Eintrags, **PR_TEMPLATEID**. Vorlagenbezeichner sollten für Einträge unterstützt werden, deren Code an Daten in einem Hostanbieter gebunden sein muss.
  
Einige Beispiele dafür, wann ein Adressbuchanbieter **IABLogon::OpenTemplateID** implementieren soll, sind wie folgt: 
  
- So aktualisieren Sie die Daten für einen kopierten Eintrag regelmäßig, damit sie mit dem Original synchronisiert bleiben.
    
- So implementieren Sie Funktionen, die der Hostanbieter nicht implementieren kann, z. B. dynamisches Auffüllen einer Liste, die in der Detailtabelle des Eintrags aus Daten auf einem Server angezeigt wird.
    
- So steuern Sie die Interaktion zwischen Eigenschaften im Eintrag des Hostanbieters und dem ursprünglichen Eintrag, z. B. das Berechnen des **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) aus den Werten der Bearbeitungssteuerelemente in der Detailanzeige, die unterschiedliche Komponenten der Adresse enthalten.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn ein Hostanbieter einen Eintrag von Ihrem Anbieter kopiert oder erstellt und Sie eine Eigenschaftsobjektimplementierung über **IABLogon::OpenTemplateID** liefern, verarbeiten Sie die meisten Aufrufe zum Verwalten des Eintrags. Da es jedoch aufgabe des Hostanbieters ist, diese Anrufe an Sie weiter zu weiterleiten, kann der Hostanbieter jeden Anruf abfangen und eine benutzerdefinierte Verarbeitung vor dem Weiterleiten des Anrufs durchführen.
  
Sie sollten die folgenden Richtlinien in Ihren Eigenschaftsobjektimplementierungen verwenden:
  
- Wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird, bestimmen Sie, ob die Anforderung für eine berechnete Eigenschaft gilt, und behandeln Sie sie, falls ja. Übertragen Sie alle Anforderungen für nicht komputierte Eigenschaften an den Hostanbieter. 
    
- Wenn [IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufgerufen wird, um eine beliebige Tabelle mit Ausnahme der Detailanzeigetabelle zu öffnen, behandeln Sie die Anforderung. Die meisten Tabellen können nicht exakt in den Hostanbieter kopiert werden. Sie müssen die **IMAPITable-Implementierung** für diese angeforderten Tabellen generieren. Die Detailtabelle **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft muss in den Hostanbieter kopiert werden. Dadurch kann dieser Anbieter die Tabelle lokal generieren. Möglicherweise möchten Sie die Implementierung der Anzeigetabelle umschließen, um Anzeigetabellebenachrichtigungen zu generieren. 
    
- Wenn [IMAPIProp::SetProps](imapiprop-setprops.md) aufgerufen wird, kann der Hostanbieter die Daten überprüfen, bevor Sie die Eigenschaften festlegen können. Sie können überprüfen, ob alle erforderlichen Eigenschaften festgelegt oder berechnet wurden. Wenn ein Fehler erkannt wird, geben Sie den entsprechenden Fehlerwert und, falls dies der Fall ist, eine weitere Erläuterung über [IMAPIProp::GetLastError zurück.](imapiprop-getlasterror.md)
    
- Wenn [IMAPIProp::SaveChanges aufgerufen](imapiprop-savechanges.md) wird, möchte der Hostanbieter möglicherweise eine Verarbeitung durchführen, bevor Sie den Eintrag speichern. Sie sollten alle Daten, die von den geänderten Eigenschaften betroffen sind, z. B. eine neue Adresse, im Eintrag des Hostanbieters speichern. 
    
Im Allgemeinen sollten Sie die Implementierung des Eintrags, den Sie an den Hostanbieter übergeben, alle Methoden abfangen, um kontextspezifische Manipulationen der relevanten Eigenschaften durchzuführen. Wenn das FILL_ENTRY im  _ulTemplateFlags-Parameter_ übergeben wird, legen Sie alle Eigenschaften für den Eintrag. 
  
Wenn Sie ein neues Eigenschaftsobjekt im  _lppMAPIPropNew-Parameter_ zurückgeben, rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) des Eigenschaftsobjekts des Hostanbieters auf, um einen Verweis zu verwalten. Alle Aufrufe über das gebundene Objekt, das von der in _lppMAPIPropNew_ zurückgegebenen **IMAPIProp-Implementierung** zurückgegeben wird, sollten an die entsprechende Methode im Hosteigenschaftsobjekt geroutet werden, nachdem sie vom gebundenen Objekt behandelt wurden. 
  
Die Eigenschafts-IDs aller benannten Eigenschaften, die über ihr gebundenes Eigenschaftsobjekt übergeben werden, befinden sich im Bezeichnernamespace Ihres Anbieters. Ihre Implementierung der [IMAPIProp::GetNamesFromIDs-Methode](imapiprop-getnamesfromids.md) sollte die Namen der Eigenschaften bestimmen, damit sie vorlagenspezifische Aufgaben ausführen kann. Ebenso müssen sich Eigenschaften, die Ihr Anbieter an den Hostanbieter weitergibt, auch in Ihrem Namespace enthalten. Wenn Sie z. B. eine benannte Eigenschaft in **OpenTemplateID** festlegen, sollten Sie einen Ihrer Bezeichner für den Namen verwenden, indem Sie sie bei Bedarf erstellen, indem Sie die [IMAPIProp::GetIDsFromNames-Methode](imapiprop-getidsfromnames.md) aufrufen. 
  
Wenn Sie den in  _lpTemplateID_ übergebenen Eintragsbezeichner nicht erkennen, geben Sie MAPI_E_UNKNOWN_ENTRYID.
  
Weitere Informationen zum Arbeiten mit Adressbuchvorlagenbezeichnern finden Sie unter [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid (kanonische Eigenschaft)](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

