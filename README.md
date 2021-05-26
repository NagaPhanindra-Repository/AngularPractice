# MCGiftCardManagementRepo
Spring boot Microservice and Angular App



----------------------------------------------------------------


package com.codemer.cardholder.model;

public class SanctionsTransactionStatus {
	private RequestHeader requestHeader;
	private String sanctionListCountry;
	private Transaction transaction;

	public RequestHeader getRequestHeader() {
	return requestHeader;
	}

	public void setRequestHeader(RequestHeader requestHeader) {
	this.requestHeader = requestHeader;
	}

	public String getSanctionListCountry() {
	return sanctionListCountry;
	}

	public void setSanctionListCountry(String sanctionListCountry) {
	this.sanctionListCountry = sanctionListCountry;
	}

	public Transaction getTransaction() {
	return transaction;
	}

	public void setTransaction(Transaction transaction) {
	this.transaction = transaction;
	}

	@Override
	public String toString() {
	StringBuilder sb = new StringBuilder();
	sb.append(SanctionsTransactionStatus.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
	sb.append("requestHeader");
	sb.append('=');
	sb.append(((this.requestHeader == null)?"<null>":this.requestHeader));
	sb.append(',');
	sb.append("sanctionListCountry");
	sb.append('=');
	sb.append(((this.sanctionListCountry == null)?"<null>":this.sanctionListCountry));
	sb.append(',');
	sb.append("transaction");
	sb.append('=');
	sb.append(((this.transaction == null)?"<null>":this.transaction));
	sb.append(',');
	if (sb.charAt((sb.length()- 1)) == ',') {
	sb.setCharAt((sb.length()- 1), ']');
	} else {
	sb.append(']');
	}
	return sb.toString();
	}


}




----------------------------------------------------------------------



package com.codemer.cardholder.model;

import java.util.List;

public class Transaction {
	private Integer transactionId;
	private List<SanctionsTransactionEntity> entities = null;

	public Integer getTransactionId() {
	return transactionId;
	}

	public void setTransactionId(Integer transactionId) {
	this.transactionId = transactionId;
	}

	public List<SanctionsTransactionEntity> getEntities() {
	return entities;
	}

	public void setEntities(List<SanctionsTransactionEntity> entities) {
	this.entities = entities;
	}

	@Override
	public String toString() {
	StringBuilder sb = new StringBuilder();
	sb.append(Transaction.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
	sb.append("transactionId");
	sb.append('=');
	sb.append(((this.transactionId == null)?"<null>":this.transactionId));
	sb.append(',');
	sb.append("entities");
	sb.append('=');
	sb.append(((this.entities == null)?"<null>":this.entities));
	sb.append(',');
	if (sb.charAt((sb.length()- 1)) == ',') {
	sb.setCharAt((sb.length()- 1), ']');
	} else {
	sb.append(']');
	}
	return sb.toString();
	}

}

	
	
	---------------------------------------------------------------------
	
	
	
	package com.codemer.cardholder.model;

public class SanctionsTransactionEntity {
	private Integer entSeqNbr;
	private String sanctionOrglMatchInd;

	public Integer getEntSeqNbr() {
	return entSeqNbr;
	}

	public void setEntSeqNbr(Integer entSeqNbr) {
	this.entSeqNbr = entSeqNbr;
	}

	public String getSanctionOrglMatchInd() {
	return sanctionOrglMatchInd;
	}

	public void setSanctionOrglMatchInd(String sanctionOrglMatchInd) {
	this.sanctionOrglMatchInd = sanctionOrglMatchInd;
	}

	@Override
	public String toString() {
	StringBuilder sb = new StringBuilder();
	sb.append(SanctionsTransactionEntity.class.getName()).append('@').append(Integer.toHexString(System.identityHashCode(this))).append('[');
	sb.append("entSeqNbr");
	sb.append('=');
	sb.append(((this.entSeqNbr == null)?"<null>":this.entSeqNbr));
	sb.append(',');
	sb.append("sanctionOrglMatchInd");
	sb.append('=');
	sb.append(((this.sanctionOrglMatchInd == null)?"<null>":this.sanctionOrglMatchInd));
	sb.append(',');
	if (sb.charAt((sb.length()- 1)) == ',') {
	sb.setCharAt((sb.length()- 1), ']');
	} else {
	sb.append(']');
	}
	return sb.toString();
	}


}

	
	
	
	
	
	------------------------------------------------
	
	
	
	public SanctionsTransactionStatus getSanctionsTransactionUpdateRequest(String memberName) {
		SanctionsTransactionStatus transactionRequest=new SanctionsTransactionStatus();
		RequestHeader requestHeader=new RequestHeader();
		requestHeader.setUserId(memberName);
		requestHeader.setSystemName("SubmissionHub");
		requestHeader.setMessageReference("3434434");
		transactionRequest.setRequestHeader(requestHeader);
		
		transactionRequest.setSanctionListCountry("USA");
		
		Transaction trx=new Transaction();
		trx.setTransactionId(3716236);
		
		List<SanctionsTransactionEntity> entities=new ArrayList<>();
		SanctionsTransactionEntity entity=new SanctionsTransactionEntity();
		entity.setEntSeqNbr(1);
		entity.setSanctionOrglMatchInd("Y");
		entities.add(entity);
		trx.setEntities(entities);
		
		transactionRequest.setTransaction(trx);
		
		
		return transactionRequest;
	}
	
	
	
	
	
	---------------------------------
	
	
