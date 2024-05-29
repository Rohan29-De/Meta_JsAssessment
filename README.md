// create a variable to hold your NFT's
const digitalAssets = []
// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function createDigitalAsset (_owner, _eyeShade, _topWear, _accessory) {

    const digitalAsset = {
        "owner": _owner,
        "eyeShade": _eyeShade,
        "topWear": _topWear,
        "accessory": _accessory
    }
    digitalAssets.push(digitalAsset);
    console.log("Minted: "+ _owner);
}

// create a "loop" that will go through an "array" of digital assets
// and print their metadata with console.log()
function displayDigitalAssets () {
    for(i=0; i<digitalAssets.length; i++){
        console.log("\nID: \t\t " +(i+1));
        console.log("Name: \t\t "+digitalAssets[i].owner);
        console.log("\nEye Color: \t "+digitalAssets[i].eyeShade);
        console.log("\nShirt Type: "+digitalAssets[i].topWear);
        console.log("\nBling: \t "+digitalAssets[i].accessory);
    }
}

// print the total number of digital assets we have minted to the console
function totalDigitalAssets() {
    console.log("\n"+digitalAssets.length);
}

// call your functions below this line
createDigitalAsset("Rohan", "Black", "Hoddie", "Gold Chain");
createDigitalAsset("Priyansh", "Blue", "jacket", "Plastic Chain");
createDigitalAsset("Rahul", "Brown", "Hoddie", "Silver Chain");
createDigitalAsset("Nikita", "Red", "Sweatshirt", "Platinum Chain");
displayDigitalAssets();
totalDigitalAssets();
