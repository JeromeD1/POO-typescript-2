import * as assert from "assert";

class BankCustomer {
    private name : string;
    private cardCode : number;

    constructor(name : string, cardCode : number) {
        this.name = name;
        this.cardCode = cardCode;
    }


    getName() : String {
        return this.name;
    }

    verifyPinInput(pinInput : number) : boolean {
        return pinInput === this.cardCode;
    }
}


const customer = new BankCustomer('John Doe', 3579);
assert.equal(typeof customer.getName, 'function');
assert.equal(typeof customer.verifyPinInput, 'function');
assert.equal(customer.getName(), 'John Doe');
assert.ok(customer.verifyPinInput(3579));
